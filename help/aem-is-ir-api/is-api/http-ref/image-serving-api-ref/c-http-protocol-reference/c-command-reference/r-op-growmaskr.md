---
description: Dilate/erode image. Tillämpar en morfologisk dilatation (radie > 0) eller erodering (radie < 0) på maskdata.
solution: Experience Manager
title: op_growthMaskR
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# op_growthMaskR{#op-growmaskr}

Dilate/erode image. Tillämpar en morfologisk dilatation (radie > 0) eller erodering (radie &lt; 0) på maskdata.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius in pixels where <span class="codeph"><span class="varname"> radiusR</span></span> is applied as is oavsett om masken nedsamplas (int -100..100). </p></td> 
 </tr> 
</table>

Används främst för att förstora eller förminska en mask något för att undvika artefakter runt maskens kant.

## Egenskaper {#section-b1c66d65168d4ea695e8662ea690bd4e}

Gäller för det aktuella lagret eller för lagret `0` om `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, utan att förändras.

## Se även {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Lagereffekter](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_growth](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growthMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
