---
description: Bild-/metadataversion. När du arbetar med innehåll som ändras ofta kan servrar i cachningsnätverk som Akamai, webbläsarcacher och cacheminnen för företagsproxyservrar lagra Image Serving-svar som kan vara inaktuella under tidsperioder.
solution: Experience Manager
title: id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# id{#id}

Bild-/metadataversion. När du arbetar med innehåll som ändras ofta kan servrar i cachningsnätverk som Akamai, webbläsarcacher och cacheminnen för företagsproxyservrar lagra Image Serving-svar som kan vara inaktuella under tidsperioder.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>Versionssträng. </p> </td> 
 </tr> 
</table>

Image Serving innehåller en versionsfunktion som kan minska risken för att en inaktuell cachepost används av ett program. Den här mekanismen innebär att du använder `req=props` för att hämta versionsidentifierarsträngar för bilddata och metadata (till exempel bildschema eller zoommåldata). Strängen för versionsidentifierare läggs sedan till i cacheable Image Serving-begäranden med kommandot `id=`.

När en källbild eller metadata ändras, ändras även motsvarande värde för versions-ID. Genom att ta med ett aktuellt version-ID-värde med kommandot `id=` säkerställer du att gamla cacheposter inte längre är tillgängliga.

I följande tabell visas de versionsidentifierarsträngar som ska användas för varje `req=`-typ:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> versionsidentifierare från req=props</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> map </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> mask </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> mål </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> användardata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` Typer som inte anges ovan har antingen en kort TTL (  `attribute::NonImgExpiration`) eller så är deras svar inte tillgängliga alls. det inte finns någon fördel med att ta  `id=` med sådana förfrågningar.

## Egenskaper {#section-62e973d0d5884abebbb0679f9278ae2c}

Begär attribut. Valfritt. Ignoreras alltid av servern.

## Standard {#section-96136720c82842c89505347ec39e6024}

Ingen.

## Exempel {#section-a5fb871e0ec8485c91c4fca78895d17f}

Se beskrivningen av [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) om du vill se syntaxhjälp.

## Se även {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [katalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [attribut::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
