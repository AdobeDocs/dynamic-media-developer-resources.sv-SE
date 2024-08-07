---
title: res
description: Materialupplösning. Anger upplösningen för den repeterbara texturen eller den dekala bilden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# res{#res}

Materialupplösning. Anger upplösningen för den repeterbara texturen eller den dekala bilden.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Upplösning; materialupplösningsenheter (vanligen pixlar per tum) (reella). </p> </td> 
 </tr> 
</table>

Om det finns ett dekalmaterial gäller `size=` om både `size=` och `res=` anges.

## Egenskaper {#section-6a458ddc202f46e0b668c9f040a65cef}

Materialattribut. Ignoreras av heltäckande färgmaterial. Endast av kabinettmaterial och fönsterbeläggningsmaterial om en textur också används.

## Standard {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, om materialet är baserat på en katalogpost, annars `attribute::Resolution`, om `res= is` inte har angetts eller angetts till ett värde som är mindre än eller lika med 0.

## Se även {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Materialupplösning](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [katalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
