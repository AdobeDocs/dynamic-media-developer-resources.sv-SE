---
description: Rektangel i slutvyn. Gör att den slutliga visningsbilden kan delas upp i flera remsor eller plattor, som kan levereras separat och rekonstrueras av klienten utan att några artefakter uppstår längs kanterna.
seo-description: Rektangel i slutvyn. Gör att den slutliga visningsbilden kan delas upp i flera remsor eller plattor, som kan levereras separat och rekonstrueras av klienten utan att några artefakter uppstår längs kanterna.
seo-title: rect
solution: Experience Manager
title: rect
topic: Scene7 Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rect{#rect}

Rektangel i slutvyn. Gör att den slutliga visningsbilden kan delas upp i flera remsor eller plattor, som kan levereras separat och rekonstrueras av klienten utan att några artefakter uppstår längs kanterna.

`rect= *``*, *``*[, *`coordsizscale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixelförskjutning från det övre vänstra hörnet av visningsbilden till det övre vänstra hörnet av visningsrektangeln (int, int), uttryckt i pixlar, efter att <span class="varname"> skala</span> har använts. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Storlek på avkastning i pixlar (int, int). Anger svarsbildens storlek. Bilden fylls med <span class="codeph"> bgc=</span> i områden som inte täcks av visningsbilden (eller vänster genomskinlighet om <span class="codeph"> fmt=*-alpha</span> finns i begäran). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Skalfaktor (verklig). Värden som är mindre än 1,0 minskar upplösningen och värden som är större än 1,0 ökar upplösningen. </p></td> 
 </tr> 
</table>

Med det här kommandot kan Image Serving leverera stora bilder via HTTP som annars skulle överskrida den storleksgräns som konfigurerats med `attribute::MaxPix`.

>[!NOTE]
>
>För bästa resultat vid JPEG-komprimering bör remsan eller plattstorleken vara en multipel av JPEG-kodningspanelens storlek (16 x 16 pixlar).

## Exempel {#section-932fcfcb41d74a29bc929e4430c49601}

Dela upp en utskrivbar CMYK-bild i flera remsor med full upplösning för att minska filstorleken för nedladdningen. Om vi begär en sammanhängande bild:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Först hämtas relevant information om bilden:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

Textsvaret innehåller följande egenskaper:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Baserat på den här informationen bestämmer vi att vi vill ha fyra 600x2000-pixelremmar. Kommandot `rect=` används för att beskriva remsornas storlek och positioner.

Eftersom den här bilden ändras ofta kommer vi att inkludera `id=` kommandot för att minimera risken att få ett eller flera remsor från en äldre version av bilden som kan ha cachelagrats i ett CDN- eller proxyserver. Värdet på `image.version` egenskapen används för detta ändamål.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Egenskaper {#section-aae223cee13e46d38b74680c048d945b}

Visa attribut. Används oavsett den aktuella lagerinställningen.

Alla områden i avkastningen som sträcker sig utanför visningsbilden läggs till med `bgc=`.

Viktigt `rect=` appliceras *efter* slutlig skalning och anpassning med `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`och `align=`.

## Standard {#section-b296d3bbfb19441f87137a452b70f19a}

Hela, oförändrad visningsbild ( `rect=0,0,width,height,1.0`).

## Se även {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)[align=,¥fit=,¥rgn=¥,¥attribute::MaxPix¥,¥id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
