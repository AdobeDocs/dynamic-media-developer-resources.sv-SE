---
title: Teckensnittshantering
description: Alla teckensnitt som refereras i RTF-strängen måste vara tillgängliga i teckensnittsmappningsfilen för standardkatalogen eller den aktuella bildkatalogen, annars returneras ett fel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Teckensnittshantering{#font-handling}

Alla teckensnitt som refereras i RTF-strängen måste vara tillgängliga i teckensnittsmappningsfilen för standardkatalogen eller den aktuella bildkatalogen, annars returneras ett fel.

Du får bäst kvalitet på kursiv och fet stil om du registrerar motsvarande teckensnittsfiler. Om den inte är tillgänglig kan servern syntetisera feta och/eller kursiva teckensnitt från standardteckensnittet. (Se [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

Teckensnittet som anges med `attribute::DefaultFont` används när ingen anges explicit i RTF-strängen.

Image Serving har stöd för TrueType, OpenType och Adobe Type 1 (endast Windows).

## Stöd för teckensnitt i Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` stöder Photofont®-teckensnitt med följande begränsningar:

* `\cf` ignoreras i textintervall där teckensnittet Photofont anges, Teckensnittet i Photoshop har fördefinierade färger
* Syntetiserade teckensnittsformat stöds inte. användning av `\b` och `\i`kräver motsvarande teckensnittsmappningsposter, annars returneras ett fel

* Lodrätt textflöde stöds inte
* Fototeckensnitt med 16-bitarsbilder stöds inte
* Fototeckensnitt med flera tecken per bild stöds inte
* Tidigare färgkonvertering används om inte färgprofiler bäddas in i fototeckensnittsbilder. i det här fallet används alltid den relativa färgorimetriska återgivningsmetoden och svartpunktskompensationen

Se [www.photofont.com](https://www.photofont.com) för ytterligare information.

## Se även {#section-6cb8a802aa044836bbe449d559093f3a}

[Referens för teckensnittskarta](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](https://www.photofont.com)
