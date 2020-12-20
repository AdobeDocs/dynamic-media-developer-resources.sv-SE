---
description: Decal size. Anger storleken på ett dekalt material.
seo-description: Decal size. Anger storleken på ett dekalt material.
seo-title: size
solution: Experience Manager
title: size
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# storlek{#size}

Decal size. Anger storleken på ett dekalt material.

` size= *`bredd,höjd`*[ *`,tjocklek`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> bredd, höjd  </span> </p> </td> 
  <td class="stentry"> <p>Storlek på det dekala objektet i scenkoordinatenheter (vanligen tum) (reella, reella). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> tjocklek  </span> </p> </td> 
  <td class="stentry"> <p>Tjocklek för det dekala objektet i scenkoordinatenheter (vanligtvis tum) (reella). </p> </td> 
 </tr> 
</table>

Om varken bredd eller höjd är 0 skalas bilden till de exakta angivna dimensionerna och bildens proportioner bevaras inte. Om du anger värdet 0 bevaras bildens proportioner.

Om *`thickness`* anges återges en skugga om vinjetteringsobjektet definierar en lämplig ljusvektor. Ange *`thickness`* till 0 om du vill inaktivera skuggåtergivning.

## Egenskaper {#section-818e01e91fed4015951189c818ef28d8}

Materialattribut. Används endast av dekaler. ignoreras av alla andra material. `res=` ignoreras om bredden eller höjden är större än 0. Värden får inte vara negativa.

## Standard {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` om det dekala materialet är baserat på en katalogpost, i annat fall  `size=0,0,0`. Dekalstorleken beräknas från `res=` om *`wid`* och *`hei`* inte har angetts eller har angetts till 0. Ingen skugga återges om *`thickness`* inte har angetts eller angetts till 0.

## Exempel {#section-04fdc2b60b9e4071b672bf6a913738ad}

En MSS för en dekal, som storleksändras baserat på upplösning, roteras 20 grader medsols och har en tjocklek på 2,5 tum för en lämplig skuggeffekt:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Se även {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Scenkoordinater](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1),  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [attribut::Upplösning](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
