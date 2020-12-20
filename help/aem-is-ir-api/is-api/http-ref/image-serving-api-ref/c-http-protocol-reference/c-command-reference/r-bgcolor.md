---
description: Lagerbakgrundsfärg. Anger bakgrundsfärgen och opaciteten för det aktuella lagret.
seo-description: Lagerbakgrundsfärg. Anger bakgrundsfärgen och opaciteten för det aktuella lagret.
seo-title: bgColor
solution: Experience Manager
title: bgColor
topic: Scene7 Image Serving - Image Rendering API
uuid: bcbd368f-d200-4b1f-8e9f-bf4d88f14b72
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# bgColor{#bgcolor}

Lagerbakgrundsfärg. Anger bakgrundsfärgen och opaciteten för det aktuella lagret.

`bgColor= *`färg`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> färg</span></span> </p> </td> 
  <td class="stentry"> <p>Grått, RGB eller CMYK-färgvärde, med eller utan alfa. </p></td> 
 </tr> 
</table>

Genomskinliga och halvgenomskinliga områden inom markeringsramen för lagret fylls med den angivna färgen* efter att *`opac=`, `rotate=` och `extend=` har använts.

## Egenskaper {#section-19dfc13e997f4a33889a1df1e4ad50b9}

Lagerattribut. Gäller för det aktuella lagret eller för lagret 0 om `layer=comp`. Ignoreras av effektlager.

*`color`* antas finnas i den arbetsfärgrymd som motsvarar pixeltypen för  *`color`*. *`color`* konverteras korrekt om den slutliga lagerbilden har en annan pixeltyp.

## Standard {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 (helt transparent).

## Exempel {#section-6e14fcf1d31e432dbdb56b9320904453}

Se [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## Se även {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423),  [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)  [rotate=¥,¥bgc=¥,¥Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
