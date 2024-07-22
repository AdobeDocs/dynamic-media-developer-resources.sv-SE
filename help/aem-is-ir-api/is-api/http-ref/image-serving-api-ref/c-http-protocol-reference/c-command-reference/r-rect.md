---
title: rect
description: Rektangel i slutvyn. Det gör att den slutliga visningsbilden kan delas upp i flera remsor eller plattor, som kan levereras separat och rekonstrueras av klienten utan skarvar, utan några artefakter längs kanterna.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# rect{#rect}

Rektangel i slutvyn. Det gör att den slutliga visningsbilden kan delas upp i flera remsor eller plattor, som kan levereras separat och rekonstrueras av klienten utan skarvar, utan några artefakter längs kanterna.

`rect= *`coord`*, *`size`*[, *`scale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">-kod</span> </p> </td> 
  <td class="stentry"> <p>Pixelförskjutning från det övre vänstra hörnet av visningsbilden till det övre vänstra hörnet av visningsrektangeln (int, int), uttryckt i pixlar, efter att <span class="varname"> scale</span> har använts. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> storlek </span> </p></td> 
  <td class="stentry"> <p>Storlek på avkastning i pixlar (int, int). Anger svarsbildens storlek. Bilden fylls med <span class="codeph"> bgc=</span> i områden som inte täcks av visningsbilden (eller vänster genomskinlig om <span class="codeph"> fmt=*-alpha</span> finns i begäran). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Skalfaktor (verklig). Värden som är mindre än 1,0 minskar upplösningen och värden som är större än 1,0 ökar upplösningen. </p></td> 
 </tr> 
</table>

Med det här kommandot kan Image Serving leverera stora bilder via HTTP som annars skulle överskrida storleksgränsen som konfigurerats med `attribute::MaxPix`.

>[!NOTE]
>
>För bästa resultat bör storleken på remsa eller plattor vara en multipel av JPEG-kodningsrutans storlek (16 x 16 pixlar) när du använder JPEG-komprimering.

## Exempel {#section-932fcfcb41d74a29bc929e4430c49601}

Dela upp en utskrivbar CMYK-bild i flera remsor med full upplösning för att minska filstorleken för nedladdningen. Om du begärde en sammanhängande bild:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Först hämtas relevant information om bilden:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

Textsvaret innehåller följande egenskaper:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Baserat på den här informationen är fyra 600x2000-pixelremsor önskade. Kommandot `rect=` används för att beskriva remsstorlekar och positioner.

Eftersom den här bilden ändras ofta inkluderas kommandot `id=`. Om du gör det minimeras risken för att få ett eller flera remsor från en äldre version av bilden som kan ha cachelagrats i ett CDN- eller proxyserver. Värdet för egenskapen `image.version` används för detta ändamål.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Egenskaper {#section-aae223cee13e46d38b74680c048d945b}

Visa attribut. Det används oavsett den aktuella lagerinställningen.

Alla områden i avkastningen som sträcker sig utanför visningsbilden läggs till med `bgc=`.

Viktigt `rect=` används *efter* slutlig skalning och anpassning med `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` och `align=`.

## Standard {#section-b296d3bbfb19441f87137a452b70f19a}

Hela, oförändrad visningsbild ( `rect=0,0,width,height,1.0`).

## Se även {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPir x](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
