---
title: skarp
description: Öka skärpan i texturen. Anger den skärpa som ska användas när materialet återges.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# skarp{#sharp}

Öka skärpan i texturen. Anger den skärpa som ska användas när materialet återges.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Ingen skärpa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
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

`sharp=1` Använder skärpa efter att materialet har renderats. `sharp=2` tillämpar skärpa efter den första skalningen av texturen, men innan den omformas till scenen. `sharp=3` tillämpar skärpa både före och efter omformningen.

Skärpealgoritmen och mängden skärpa och andra USM-parametrar (oskarp maskering) styrs av standardmaterialmallen som tillhandahålls av vinjetteringen eller med `rs=`.

## Egenskaper {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Materialattribut. Ignoreras av heltäckande färgmaterial.

## Standard {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, om materialet är baserat på en katalogpost, annars `attribute::Sharp`.

## Se även {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[katalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
