---
description: Öka skärpan i texturen. Anger den skärpa som ska användas vid återgivning av det här materialet.
seo-description: Öka skärpan i texturen. Anger den skärpa som ska användas vid återgivning av det här materialet.
seo-title: skarp
solution: Experience Manager
title: skarp
topic: Scene7 Image Serving - Image Rendering API
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---


# skarp{#sharp}

Öka skärpan i texturen. Anger den skärpa som ska användas vid återgivning av det här materialet.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Ingen skärpa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Normal skärpa (sen). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 alternativ skärpa (tidig). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Mer skärpa (tidigt och sent). </p> </td> 
 </tr> 
</table>

`sharp=1` tillämpar skärpa efter att materialet har renderats,  `sharp=2` tillämpar skärpa efter ursprunglig skalning av texturen, men innan den omvandlas till scenen,  `sharp=3` använder skärpa både före och efter omformningen.

Skärpealgoritmen och mängden skärpa och andra USM-parametrar (oskarp maskering) styrs av standardmaterialmallen som tillhandahålls av vinjetteringen eller med `rs=`.

## Egenskaper {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Materialattribut. Ignoreras av heltäckande färgmaterial.

## Standard {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, om materialet är baserat på en katalogpost, i annat fall  `attribute::Sharp`.

## Se även {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[katalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
