---
title: Sharp
description: Standardmaterialskärpa. Anger standardläget för materialskärpa om en viss katalogpost inte innehåller ett giltigt värde för katalogskärpa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 4%

---

# Sharp{#sharp}

Standardmaterialskärpa. Anger standardläget för materialskärpa om en viss katalogpost inte innehåller ett giltigt `catalog::Sharp`-värde.

## Egenskaper {#section-dcb810d01b8a40eb991d555a3cbe48b9}

Enum.

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
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
  <td class="stentry"> <p>Mer skärpa (både före och efter omformningen). </p> </td> 
 </tr> 
</table>

## Standard {#section-613130fca7c04ce7a7734265f27aa1ea}

Ärvs från `default::Sharp` om inte definierad eller om tom.

## Se även {#section-7771824f2822443ab0297e8793bb48ae}

[katalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a), [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
