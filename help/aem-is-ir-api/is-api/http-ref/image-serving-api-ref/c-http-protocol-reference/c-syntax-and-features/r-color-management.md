---
title: Färghantering för bildhantering
description: Image Serving stöder konvertering av färgrymder baserat på färgrymdsprofiler som uppfyller ICC-specifikationen (International Color Consortium).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1220'
ht-degree: 0%

---

# Färghantering för bildhantering{#image-serving-color-management}

Image Serving stöder konvertering av färgrymder baserat på färgrymdsprofiler som uppfyller ICC-specifikationen (International Color Consortium).

## Standardfärgrymder {#section-8cfe60808bce49968091995e4e521dba}

Varje bildkatalog (och standardkatalogen) kan definiera en uppsättning ICC-profiler som utgör standardfärgmodellerna för den här katalogen - en indata och en utdataprofil för gråskale-, RGB- och CMYK-data. Se
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Färgrymd för indata {#section-9f08e2c1b6aa4fe4815be174972c1944}

Source-bilder kan bädda in ICC-profiler för att definiera indatafärgrymden. Om ingen profil är inbäddad i en källbild används `attribute::IccProfileSrc*` av den tillämpliga bildkatalogen som motsvarar källbildens pixeltyp. Om det här attributet inte är definierat i bildkatalogen används `attribute::IccProfile*`. Om det katalogattributet inte heller är definierat färghanteras inte bilden och endast naiva omformningar används.

## Färgrymd för utdata {#section-b517bca622b64dcfa7defba6035d0716}

Färgrymden för det slutliga bildresultatet av en begäran definieras med kommandot `icc=`. Om `icc=` inte anges används standardutdatafärgrymden (från begärans huvudkatalog) som motsvarar pixeltypen för utdatafärgen som utdatafärgrymd. Om ingen utdataprofil har definierats i huvud- eller standardkatalogen och om baslagret är en bild med en inbäddad profil som matchar utdatapixeltypen, används den profilen för utdatafärgrymden. I annat fall förblir utdatafärgrymden odefinierad - endast naiva färgkonverteringar används vid konvertering mellan pixeltyper och ingen färgprofil kan bäddas in i utdatabilden.

Utdatafärgrymden för en kapslad/inbäddad bildserverförfrågan är alltid densamma som utdatafärgrymden för den yttre inbäddningsbegäran.

## Solida färger {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Färgvärden som anges med `color=`, `bgcolor=` eller RTF-kommandot `\iscolortbl` associeras med indatafärgrymden om färgvärdet innehåller suffixet S, annars associeras de med utdatafärgrymden. Färgvärden som anges med `bgc=` eller RTF-kommandona `\colortbl` och `\cmykcolortbl` associeras alltid med motsvarande standardfärgrymd eller faktiska utdatafärgrymd.

>[!NOTE]
>
>För närvarande deltar `bgc=` inte fullt ut i färghanteringen. S-suffixet ignoreras när det anges med `bgc=` och naiv konvertering tillämpas när pixeltypen för färgvärdet som anges med `bgc=` skiljer sig från pixeltypen för utdatabilden. Annars är `bgc=` associerat med den faktiska utdatafärgrymden.

## Kapslade och inbäddade begäranden {#section-bdda638c31504f26a77e51ebb1ea6e3b}

Utdatafärgrymden för kapslade IS-begäranden och inbäddade IR-begäranden anges automatiskt till den yttersta begärans utdatafärgrymd, såvida inte den kapslade begäran anger en explicit utdatafärgrymd med `icc=`. Dessutom ärver kapslade/inbäddade begäranden standardfärgrymderna för utdata från huvudkatalogen i den yttersta begäran, vilket ger en konsekvent hantering av heltäckande färgvärden.

## Konvertering av färgrymd {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Image Serving försöker vanligtvis fördröja färgkonverteringar under bearbetningen. Om alla lager i en bild har samma lagerfärgrymd konverteras till utdatafärgrymden efter sammanslagningen och den slutliga skalningen. Om det finns flera färgrymder för lager omvandlas varje lager till utdatafärgrymden innan de läggs samman.

>[!NOTE]
>
>Kommandona `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` och `op_saturation=` är RGB. De här åtgärderna bevarar endast färgåtergivningen om lagerfärgrymden har pixeltypen RGB. Om det inte är RGB konverteras data till RGB med tidigare okänd färgkonvertering och resultatet har begränsad färgåtergivning. Lagerfärgrymden för sådana lager bör betraktas som obestämd.

Färgkonverteringsalternativen anges med `icc=` eller, om `icc=` inte anges, med `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` och `attribute::IccDither`.

## Bädda in färgprofiler {#section-261ebbae5ce046589a776ca972380052}

ICC-färgprofilen för utdatafärgrymden, om den är tillgänglig, kan bäddas in i svarsbilden genom att ange `iccEmbed=`.

## Hantera ICC-profiler {#section-eb210e4b44e64e2c8b80ee59216c5555}

Alla färgprofiler som används av servern måste överensstämma med ICC-specifikationen. ICC-profilfiler har vanligtvis filsuffixet [!DNL .icc] eller [!DNL .icm] och finns tillsammans med bilddatafiler.

Utdataprofiler kan anges med filsökväg/namn i kommandot `icc=`, men du bör registrera alla profilfiler i ICC-profilkartan i standardkatalogen eller bildkatalogen och använda genvägsidentifierare ( `icc::Name`) i stället för filsökvägar.

Alla ICC-profiler som refereras i `catalog::IccProfile` och i `attribute::IccProfile*` måste registreras i ICC-profilkartan för bilden eller standardkatalogen.

## Begränsningar {#section-fb50ede40b124b89b30679da29782ab5}

För närvarande stöds endast färgrymderna CMYK, RGB och gråskala.

## ICC-färgprofiler som ingår {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Bildredigering innehåller de flesta vanliga Adobe ICC-profiler i standardbildkatalogen. Dessa profiler kan nås antingen med deras gemensamma namn (till exempel enligt Photoshop) eller med en något kortare identifierare. I följande tabell visas alla vanliga ICC-profiler. När en profil i kommandot `icc=` refereras med sitt vanliga namn måste blanksteg kodas som `%20`.

Ytterligare profiler kan läggas till i standardprofilerna, antingen i standardkatalogen eller i en viss bildkatalog. Mer information finns i [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c).

>[!NOTE]
>
>Följande tabell gäller endast för *Dynamic Media Hybrid* (körs i körläge `dynamicmedia`).

| Identifierare | Gemener | Filnamn |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | CIE RGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb-färgrymdsprofil.icm |
| `WideGamutRGB` | Bred färgomfång RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 - standard-CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 - standard-CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Web Coated SWOP 2006 Grade 3 Paper | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Web Coated SWOP 2006 Grade 5 Paper | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

Följande tabell gäller för *Dynamic Media Classic Image Serving* och *Dynamic Media* (körs i `dynamicmedia_scene7` körningsläge).

| Identifierare | Gemener | Filnamn |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRgb-färgrymdsprofil.icm |
| `WideGamutRGB` | Bred färgomfång RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 - standard-CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 - standard-CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Web Coated SWOP 2006 Grade 3 Paper | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Web Coated SWOP 2006 Grade 5 Paper | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## Se även {#section-39159397e80b4efca5f631eab8b9aa06}

[Internationellt färgkonsortier](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::Icc ccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
