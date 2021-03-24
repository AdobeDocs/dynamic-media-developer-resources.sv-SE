---
description: Materialrotationsvinkel. Definierar rotationsvinkeln för material.
solution: Experience Manager
title: rotera
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# rotera{#rotate}

Materialrotationsvinkel. Definierar rotationsvinkeln för material.

` rotate= *`vinkel`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> vinkel  </span> </p> </td> 
  <td class="stentry"> <p>Rotationsvinkel i grader (reell). </p> </td> 
 </tr> 
</table>

Rotera repeterbara texturmaterial (exklusive tapeter) i multipler av 45 grader när de används på platta objekt eller planobjekt.

Rotera repeterbara texturmaterial i godtyckliga vinklar när de används på flödeslinje- och Sketch-objekt.

Rotera material i olika vinklar.

Positiva vinklar roterar medsols. Texturen eller den dekala formen roteras runt fästpunkten ( `anchor=`); fästpunkten förblir justerad mot målobjektets nollpunkt.

## Egenskaper {#section-ad4d07897ca24f63af1a4062f8618e36}

Materialattribut. Ignoreras av enfärgat, tapet, skåp och fönsterhanteringsmaterial. *`angle`* måste vara en multipel av 45 för repeterbara texturer, såvida det inte tillämpas på flödeslinje- eller Sketch-objekt.

## Standard {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, utan rotering.

## Se även {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
