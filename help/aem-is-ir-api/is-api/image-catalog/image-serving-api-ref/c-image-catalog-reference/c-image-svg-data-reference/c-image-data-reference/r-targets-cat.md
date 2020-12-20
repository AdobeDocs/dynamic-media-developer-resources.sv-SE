---
description: Zooma måldata. Inga eller fler zoommålsegenskaper, som kan användas tillsammans med zoomvisningsprogramklienten.
seo-description: Zooma måldata. Inga eller fler zoommålsegenskaper, som kan användas tillsammans med zoomvisningsprogramklienten.
seo-title: Målgrupper
solution: Experience Manager
title: Målgrupper
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# Målgrupper{#targets}

Zooma måldata. Inga eller fler zoommålsegenskaper, som kan användas tillsammans med zoomvisningsprogramklienten.

Servern returnerar innehållet i det här fältet som svar på `req=targets`, efter att postterminatortoken `??` har ersatts.

Upp till fyra egenskaper kan kopplas till varje zoommål:

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`vänster,övre,bredd,höjd`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>Zoommålnummer (int). Zoommål måste numreras sekventiellt och i följd, med början från 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valfritt bildrute-/sidnummer för en viss ram/sida i en snurra eller broschyruppsättning. Standardvärdet är 0 om det inte anges för användning i snurra- och broschyrvisningsprogram. ignoreras av zoomvisningsprogrammet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vänster, övre  </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixelförskjutning från bildens övre vänstra hörn till det övre vänstra hörnet av zoommålrektangeln (int, int). måste vara 0 eller större. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> bredd, höjd  </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixelstorlek för zoommålrektangeln (int, int); måste vara större än 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>Textdatavärde; kan användas som textetikett för en zoommållänk. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>Textdatavärde; kan användas för att skicka målspecifik information till klienten, till exempel ett SKU-värde eller en hot-link-URL. </p> </td> 
 </tr> 
</table>

Mål. *`num`*.rect krävs för varje zoommål och måste ange en rektangel som är helt inuti bilden. Alla andra egenskaper är valfria.

*`label`* och  *`userData`* deltar i textsträngslokalisering. Mer information finns i [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) i *HTTP-protokollreferens*.

För program som använder snurra- och broschyrvisningsprogram måste zoommålen definieras i samma katalogpost som definierar bilduppsättningen. Alla zoommåldefinitioner i katalogposterna för medlemmarna i bilduppsättningen ignoreras av visningsprogrammet.

Scene7-visningsprogrammen förväntar sig zoommål i koordinaterna för den högupplösta bilden som redan har justerats med kommandona från `catalog::Modifier`.

## Egenskaper {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Egenskapens ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) datavärde.

## Standard {#section-feab29f6575e482391086a57f547543c}

Ingen.

## Se även {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[katalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [katalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), lokalisering av  [textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
