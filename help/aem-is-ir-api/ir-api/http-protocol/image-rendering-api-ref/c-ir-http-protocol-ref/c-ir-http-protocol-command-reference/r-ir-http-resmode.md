---
title: resMode
description: Omsamplingsläge. Väljer den omsamplings- och/eller interpoleringsalgoritm som ska användas för att skala den återgivna bilden till den storlek som anges med wid=, hei= eller scl=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# resMode{#resmode}

Omsamplingsläge. Väljer den omsamplings- och/eller interpoleringsalgoritm som ska användas för att skala den återgivna bilden till den storlek som anges med `wid=`, `hei=` eller `scl=`.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Väljer standardbilinjär interpolation. Den snabbaste omsamplingsmetoden. Vissa aliasing-artefakter kan bli märkbara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Väljer bikubisk interpolation. Processorintensivare än bilinjär interpolation, men ger skarpare bilder med mindre framträdande aliasartefakter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Väljer en modifierad Lanczos Window-funktion som en interpoleringsalgoritm. Kan ge något tydligare resultat än bikubisk till en högre CPU-kostnad. </p> <p> <span class="codeph"> sharp </span> har ersatts med <span class="codeph"> sharp2 </span> som har en mindre sannolikhet att orsaka aliasartefakter, även kallat Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Väljer standardomsamplingen <span class="keyword"> Adobe Photoshop </span> för att minska bildstorleken, som kallas"bikubisk skarpare" i <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-ea7029f37e094d9cb85646b85fbac0ce}

Kan inträffa var som helst i begäran. Ignoreras om ingen slutlig bildskalning används.

## Standard {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Se även {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
