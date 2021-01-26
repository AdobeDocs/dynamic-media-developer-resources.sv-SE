---
description: Oskarp mask. Oskarp maskerar lagret eller den slutliga visningsbilden, efter all skalning, om layer=comp.
seo-description: Oskarp mask. Oskarp maskerar lagret eller den slutliga visningsbilden, efter all skalning, om layer=comp.
seo-title: op_usm
solution: Experience Manager
title: op_usm
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c647e063-2405-489b-b14d-a70638ac8af7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# op_usm{#op-usm}

Oskarp mask. Oskarp maskerar lagret eller den slutliga visningsbilden, efter all skalning, om layer=comp.

Parametrarna antas gälla för bilden med full upplösning och skalas ned när en nedsamplad bild bearbetas.

`op_usm= *``*[, *``*[, *``*[, *`mängd traditionusthresholdDmonokrom`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> belopp</span></span> </p></td> 
  <td class="stentry"> <p>Filterstyrkefaktor (verklig 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radie</span></span> </p></td> 
  <td class="stentry"> <p>Filtrera kernelradien i pixlar (verklig 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> tröskelvärde</span></span> </p></td> 
  <td class="stentry"> <p>Filtertröskelnivå (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monokrom</span></span> </p></td> 
  <td class="stentry"> <p>Ange 0 för varje färgkomponent separat eller 1 för att endast tillämpa bildens intensitet (intensitet). </p> <p> <span class="codeph"><span class="varname"> Monokromeis </span></span> ignoreras för gråskalebilder. </p></td> 
 </tr> 
</table>

Lagermasken eller den sammansatta masken blir också skarpare.

## Egenskaper {#section-fb5311b34d164946b74dadb32359518a}

Lagerattribut eller vyattribut. Gäller det aktuella lagret eller den slutliga visningsbilden om `layer=comp`. Ignoreras av effektlager.

## Standard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` utan oskarp maskningseffekt.

## Se även {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
