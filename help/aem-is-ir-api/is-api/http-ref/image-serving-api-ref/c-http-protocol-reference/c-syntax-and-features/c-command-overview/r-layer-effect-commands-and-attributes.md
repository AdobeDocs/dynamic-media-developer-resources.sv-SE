---
description: Dessa kommandon kan användas för att definiera lagereffekter som skugg- och glödeffekter. Effektlager ignorerar alla andra kommandon.
solution: Experience Manager
title: Effektkommandon för lager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 483b1f24-9cd2-45e0-9d18-0dc0fbe8abcf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# Effektkommandon för lager{#layer-effect-commands}

Dessa kommandon kan användas för att definiera lagereffekter som skugg- och glödeffekter. Effektlager ignorerar alla andra kommandon.

<table id="simpletable_3094B9783772437FAACF9B382F7A32EE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode </a> </p></td> 
  <td class="stentry"> <p>Anger lagerblandningsläget. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> färg </a> </p></td> 
  <td class="stentry"> <p>Anger huvudeffektens färg och opacitet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135" type="reference" format="dita" scope="local"> effekt </a> </p></td> 
  <td class="stentry"> <p>Startar effektlagersegmentet och anger z-ordningen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464" type="reference" format="dita" scope="local"> maskUse</a> </p></td> 
  <td class="stentry"> <p>Anger hur den överordnade objektets lagermask (alfakanal) ska användas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>Fjädrar effekten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a" type="reference" format="dita" scope="local"> op_growth</a> </p></td> 
  <td class="stentry"> <p>Förstorar eller förminskar lagereffekten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_noise</a> </p></td> 
  <td class="stentry"> <p>Lägger till brus i effekten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>Minskar lageropaciteten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>Placerar effektlagret i förhållande till dess överordnade lager. </p></td> 
 </tr> 
</table>
