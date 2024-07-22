---
title: rotera
description: Materialrotationsvinkel. Definierar rotationsvinkeln för material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# rotera{#rotate}

Materialrotationsvinkel. Definierar rotationsvinkeln för material.

` rotate= *`vinkel`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> vinkel </span> </p> </td> 
  <td class="stentry"> <p>Rotationsvinkel i grader (reell). </p> </td> 
 </tr> 
</table>

Rotera repeterbara texturmaterial (utom tapeter) i multipler av 45° när det används på platta objekt eller planobjekt.

Rotera repeterbara texturmaterial i godtyckliga vinklar när de används på flödeslinje- och Sketch-objekt.

Rotera dekala material i valfri vinkel.

Positiva vinklar roterar medsols. Texturen eller den dekala roteras runt fästpunkten ( `anchor=`). Fästpunkten förblir justerad mot målobjektets ursprung.

## Egenskaper {#section-ad4d07897ca24f63af1a4062f8618e36}

Materialattribut. Ignoreras av enfärgat, tapet, skåp och fönsterhanteringsmaterial. *`angle`* måste vara en multipel av 45 för repeterbara texturer, såvida inte detta tillämpas på flödeslinje- eller Sketch-objekt.

## Standard {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, utan rotering.

## Se även {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
