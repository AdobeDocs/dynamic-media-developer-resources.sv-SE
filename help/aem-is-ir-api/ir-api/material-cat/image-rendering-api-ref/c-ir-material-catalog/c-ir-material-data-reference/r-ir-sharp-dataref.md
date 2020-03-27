---
description: Skärpa. Skärpeattribut, anger när materialet ska göras skarpare under återgivningen.
seo-description: Skärpa. Skärpeattribut, anger när materialet ska göras skarpare under återgivningen.
seo-title: Sharp
solution: Experience Manager
title: Sharp
topic: Scene7 Image Serving - Image Rendering API
uuid: f153f496-f2c5-43d0-a7f0-00045fd96af8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sharp{#sharp}

Skärpa. Skärpeattribut, anger när materialet ska göras skarpare under återgivningen.

Skärpetypen och mängden skärpa styrs av vinjetteringen via en standardmaterialmall eller med `catalog::RenderSettings`.

## Egenskaper {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Ingen skärpa. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Normal skärpa (efter omformningen). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alternativ skärpa (före omformningen). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Mer skärpa (både före och efter omformningen). </p></td> 
 </tr> 
</table>

Ignoreras av heltäckande färgmaterial, valfritt för alla andra material.

## Standard {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` används om fältet inte finns, om det är tomt eller om värdet inte är ett av de alternativ som stöds.

## Se även {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
