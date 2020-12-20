---
description: Miniatyrbildstyp. Beskriver hur en miniatyrbild för den här bilden ska skapas.
seo-description: Miniatyrbildstyp. Beskriver hur en miniatyrbild för den här bilden ska skapas.
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
topic: Scene7 Image Serving - Image Rendering API
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# ThumbType{#thumbtype}

Miniatyrbildstyp. Beskriver hur en miniatyrbild för den här bilden ska skapas.

Följande miniatyrbildstyper stöds:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Beskär (1) </p></td> 
  <td class="stentry"> <p>Beskär bilden till miniatyrbildens proportioner. Om inte proportionerna för miniatyrrektangeln och bilden är exakt likadana beskärs en del av bilden så att hela miniatyrrektangeln fylls med bilddata. Beskärningsrektangeln placeras i bilden med <span class="codeph">-attributet::ThumbHorizAlign</span> och <span class="codeph">-attributet::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Anpassa (2) </p></td> 
  <td class="stentry"> <p>Anpassa hela bilden till miniatyrrektangeln. Bilden placeras inuti miniatyrbildsrektangeln med <span class="codeph">-attributet::ThumbHorizAlign</span> och <span class="codeph">-attributet::ThumbVertAlign</span>, och allt extra utrymme fylls med <span class="codeph">-attributet::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Textur (3) </p></td> 
  <td class="stentry"> <p>Beskär bilden baserat på upplösning. Bilden skalas efter förhållandet <span class="codeph"> katalog::ThumbRes</span> till <span class="codeph"> katalog::Upplösning</span>. Om den resulterande bilden är större än miniatyrbilden beskärs den så att den får plats. Om den skalförändrade bilden är mindre än miniatyrbilden fylls det återstående området med attributet <span class="codeph">::ThumbBkgColor</span>. <span class="codeph"> attribute::</span> ThumbHorizAlignand  <span class="codeph"> attribute::</span> ThumbVertAlignin som används för att bestämma positionen för beskärningsrektangeln i en större bild eller position för en mindre bild i miniatyrbilden. </p></td> 
 </tr> 
</table>

Klienter begär miniatyrbilder med `req=tmb`-begäranden.

## Egenskaper {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Uppräkningsvärde. Giltiga värden är 1, 2 eller 3, vilket motsvarar typerna Beskär, Anpassa och Textur.

## Standard {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` används om fältet inte finns, om värdet är 0 eller om fältet är tomt.

## Se även {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ,  [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e),  [attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691),  [attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f),  [catalog::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69),  [catalog::ResolutionSure,¥req=tmbSureStruStru](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)  [ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)  [, String, Skalning av miniatyrbilder](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
