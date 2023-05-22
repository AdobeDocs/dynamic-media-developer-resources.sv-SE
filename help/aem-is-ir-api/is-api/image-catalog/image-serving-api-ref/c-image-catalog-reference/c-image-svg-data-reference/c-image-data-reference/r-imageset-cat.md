---
description: Bilduppsättningsdata. Innehåller en mekanism för att definiera sorterade uppsättningar bilder och kontrollattribut som används av Dynamic Media-visningsprogram.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# ImageSet{#imageset}

Bilduppsättningsdata. Innehåller en mekanism för att definiera sorterade uppsättningar bilder och kontrollattribut som används av Dynamic Media-visningsprogram.

En bilduppsättning består av en sorterad, kommaavgränsad lista med objekt, där varje objekt består av ett eller flera underobjekt (bild-ID, färgrute-ID, mediafilsökvägar, etiketter osv.), separerade med semikolon och/eller kolon.

Klammerparenteser `{ }` och parenteser `( )` kan användas för att avgränsa visst innehåll (till exempel färgvärden) eller för att ange kapslade uppsättningar. Klammerparenteser och parenteser som används på det här sättet får inte kodas och måste alltid visas som matchade par, annars inträffar ett katalogtolkningsfel.

>[!NOTE]
>
>Följande tecken används som angivna avgränsare och måste HTTP-kodas när de visas i uppsättningen som en del av id- eller strängvärden:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Mer information om hur du strukturerar och använder bilduppsättningar finns i dokumentationen för visningsprogram för bildservrar.

Servern returnerar innehållet i det här fältet utan ändringar som svar på en `req=imageset` begäran.

## Standarduppsättningar {#section-5ecc8ffee7224668b63f601383665564}

Följande uppsättningsdefinitioner stöds internt av Image Serving, och för vissa visningsprogram används parsning, validering och bearbetning av uppsättningen på serversidan. Varje uppsättningstyp kan identifieras genom att ange motsvarande värde i `catalog::AssetType`.

**Grundläggande färgruteuppsättningar**

Varje objekt i en grundläggande färgruteuppsättning består av en referens till en bildpost och en valfri separat referens till en bildpost som används som en färgruta.

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`färgruta`*]` |
| `*`färgruta`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS-bildreferens (katalog/id) |
| `*`swatchId`*` | IS-bildreferens (katalog/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`label`*]'}'` |
| `*`rrggbb`*` | 6-siffrigt hexadecimalt RGB färgvärde för enfärgade färgrutor |
| `*`label`*` | Valfri textetikett för heltäckande färgrutor |

**Hierarkiska färgruteuppsättningar**

Varje objekt i en hierarkisk färgruteuppsättning kan bestå av ett grundläggande färgruteobjekt eller en referens till en post i en färgruteuppsättning (färgrutor krävs för sådana objekt).

| `*`hierarkiskFärgrutaUppsättning`*` | `*`hierarkisktSwatchItem`* &#42;[ ',' *`hierarkisktSwatchItem`* ]` |
|---|---|
| `*`hierarkisktSwatchItem`*` | `*`swatchItem`* | { *`basicSwatchSetId`* ';' *`färgruta`* }` |
| `*`basicSwatchSetId`*` | IS reference (catalog/id) to a catalog record defining a basic swatch set |

**Grundläggande snurruppsättningar**

En grundläggande snurruppsättning består av en enkel lista med bild-ID:n.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Tvådimensionella snurruppsättningar**

Varje objekt i en tvådimensionell snurra kan bestå av en enkel bild, en referens till en grundläggande snurra eller en grundläggande snurra som avgränsas av klammerparenteser. Parenteser kan användas i stället för klammerparenteser.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | IS reference (catalog/id) to a catalog record defining a basic spin set |

**Siduppsättningar**

Varje objekt i en siduppsättning kan bestå av upp till tre sidbilder, åtskilda med kolon.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Medieuppsättningar**

Varje objekt i en medieuppsättning kan bestå av en bild, grundläggande färgruteuppsättning, hierarkisk färgruteuppsättning, grundläggande rotationsuppsättning, tvådimensionell rotation, siduppsättning eller videoresurs. Varje medieuppsättningsobjekt kan också innehålla en valfri färgruta och en typidentifierare.

| `*`mediaSet`*` | `*`artikel`* &#42;[ , *`artikel`* ]` |
|---|---|
| `*`artikel`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`reserverad`* ] ] ]` |
| `*`videoItem`*` | `*`video`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`recut`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | IS-bild-ID |
| `*`video`*` | Filsökväg för video/animering eller statiskt katalog-ID |
| `*`recut`*` | Sökväg till XML-fil för postdefinition eller statiskt katalog-ID |
| `*`imageId`*` | IS-bild-ID |
| `*`setId`*` | IS reference to image, spin, or ecatalog set |
| `*`inlineSet`*` | Infogad bild, snurra eller katalog |
| `*`reserverad`*` | Reserverad för framtida bruk |

**Videouppsättningar**

En videouppsättning består av en enkel lista med video-ID där varje id refererar till en post i den statiska innehållskatalogen.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Egenskaper {#section-17c731e5c46646aa90ac21f39bb693ca}

Textsträng. Kommaavgränsad lista med `catalog::Id` värden, absoluta sökvägar för Image Server-filer eller sökvägar i förhållande till `attribute::RootPath`. Samma bild kan refereras flera gånger i uppsättningen. Den definierande katalogposten kan visas i uppsättningen på vilken plats som helst.

Det här fältet deltar i textsträngslokalisering. Förutom *`label`* strängar (del av *`solidColorSpecifier`*) lokaliseras alla avgränsade fält om de innehåller minst ett &#39; `^loc=…^`&#39; lokaliseringstoken. Se [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) i *HTTP-protokollreferens* för mer information.

## Standard {#section-c3a60e360393478284f0f2d2da5b963b}

Ingen.

## Se även {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Översättning av objekt-ID](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Dokumentation för bildvisning
