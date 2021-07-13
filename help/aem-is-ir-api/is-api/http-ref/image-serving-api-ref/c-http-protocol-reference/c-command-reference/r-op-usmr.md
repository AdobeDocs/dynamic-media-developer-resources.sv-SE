---
description: Oskarp mask. Oskarp maskerar lagret eller den slutliga visningsbilden, efter all skalning, om layer=comp.
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# op_usmR{#op-usmr}

Oskarp mask. Oskarp maskerar lagret eller den slutliga visningsbilden, efter all skalning, om layer=comp.

Parametrarna används som de är, oavsett om nedsampling har skett eller inte.

`op_usmR= *``*[, *``*[, *``*[, *`amountTradiusRthresholdDmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> belopp</span></span> </p></td> 
  <td class="stentry"> <p>Filterstyrkefaktor (verklig 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Filtrera kernelradien i pixlar (verklig 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> tröskelvärde</span></span> </p></td> 
  <td class="stentry"> <p>Filtertröskelnivå (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monokrom</span></span> </p></td> 
  <td class="stentry"> <p>Ange 0 för varje färgkomponent separat eller 1 för att endast tillämpa bildens intensitet (intensitet). </p> <p><span class="codeph"> <span class="varname"> Monokromeis </span></span> ignoreras för gråskalebilder. </p> </td> 
 </tr> 
</table>

Lagermasken eller den sammansatta masken blir också skarpare.

## Egenskaper {#section-fb5311b34d164946b74dadb32359518a}

Lagerattribut eller vyattribut. Gäller det aktuella lagret eller den slutliga visningsbilden om `layer=comp`. Effektlager ignorerar det.

## Standard {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` utan oskarp maskningseffekt.

## Se även {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
