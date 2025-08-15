---
description: Zooma måldata. Inga eller fler zoommålsegenskaper, som kan användas tillsammans med zoomvisningsprogramklienten.
solution: Experience Manager
title: Målgrupper
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Målgrupper{#targets}

Zooma måldata. Inga eller fler zoommålsegenskaper, som kan användas tillsammans med zoomvisningsprogramklienten.

Servern returnerar innehållet i det här fältet som svar på `req=targets`, efter att postavslutningstoken för `??` har ersatts.

Upp till fyra egenskaper kan kopplas till varje zoommål:

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`left,top,width,height`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Zoommålnummer (int). Zoommål måste numreras sekventiellt och sekventiellt, med början med 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame </span> </span> </p> </td> 
  <td class="stentry"> <p>Valfritt bildrute-/sidnummer för en viss bildruta/sida i en snurra eller broschyruppsättning. Standardvärdet är 0 om det inte anges för användning av snurra- och broschyrvisningsprogram, ignoreras av zoomningsvisningsprogrammet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vänster, överst </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixelförskjutning från bildens övre vänstra hörn till det övre vänstra hörnet av zoommålrektangeln (int, int); måste vara 0 eller större. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width, height </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixelstorleken för zoommålrektangeln (int, int); måste vara större än 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span> </span> </p> </td> 
  <td class="stentry"> <p>Textdatavärde; kan användas som textetikett för en zoommållänk. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Textdatavärde; kan användas för att skicka målspecifik information till klienten, t.ex. ett SKU-värde eller en URL med hot-link. </p> </td> 
 </tr> 
</table>

Mål. *`num`*.rect krävs för varje zoommål och måste ange en rektangel helt inuti bilden. Alla andra egenskaper är valfria.

*`label`* och *`userData`* deltar i textsträngslokalisering. Mer information finns i [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) i *HTTP-protokollreferens*.

För program som använder snurra- och broschyrvisningsprogram måste zoommålen definieras i samma katalogpost som definierar bilduppsättningen. Alla zoommåldefinitioner i katalogposterna för medlemmarna i bilduppsättningen ignoreras av visningsprogrammet.

Visningsprogram för dynamiska media förväntar sig zoommål i koordinaterna för den högupplösta bilden som redan har justerats med kommandona från `catalog::Modifier`.

## Egenskaper {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Egenskapsdatavärde](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md).

## Standard {#section-feab29f6575e482391086a57f547543c}

Ingen.

## Se även {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[katalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [katalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
