---
description: Dilate/erode image. Tillämpar en morfologisk dilatation (radie > 0) eller erodering (radie < 0) på maskdata.
seo-description: Dilate/erode image. Tillämpar en morfologisk dilatation (radie > 0) eller erodering (radie < 0) på maskdata.
seo-title: op_growthMask
solution: Experience Manager
title: op_growthMask
topic: Scene7 Image Serving - Image Rendering API
uuid: 016501e8-33c5-4c9e-8d26-120b1e929c55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# op_growthMask{#op-growmask}

Dilate/erode image. Tillämpar en morfologisk dilatation (radie > 0) eller erodering (radie &lt; 0) på maskdata.

`op_growMask= *`radie`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radie</span> </p> </td> 
  <td class="stentry"> <p>Dilate/erode radius in pixels, där radius antas gälla för masken med full upplösning och därför skalas ned för masker med nedsampling (int -100..100). </p></td> 
 </tr> 
</table>

Används främst för att förstora eller förminska en mask något för att undvika artefakter runt maskens kant.

## Egenskaper {#section-b1c66d65168d4ea695e8662ea690bd4e}

Gäller för det aktuella lagret eller för lagret `0` om `layer=comp`.

## Standard {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, utan att förändras.

## Se även {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Lagereffekter](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_growth](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growthMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
