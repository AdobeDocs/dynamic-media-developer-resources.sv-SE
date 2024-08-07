---
title: op_growth
description: Dilate/erode image. Använder en morfologisk dilat (radie > 0) eller erodera (radie < 0) på bilddata.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# op_growth{#op-grow}

Dilate/erode image. Använder en morfologisk dilat (radie > 0) eller erodera (radie &lt; 0) på bilddata.

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius in pixels (int -100..100). </p></td> 
 </tr> 
</table>

`*`radius`*` är i pixlar i förhållande till den sammansatta bilden. Om bilden är färgad bearbetas varje komponent separat.

Används främst för att ändra storlek på lagereffekter. Det är också användbart om du vill få specialeffekter på textlager eller enfärgade lager med masker.

## Egenskaper {#section-b1c66d65168d4ea695e8662ea690bd4e}

Lagerattribut. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, utan ändring.

## Se även {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Lagereffekter](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
