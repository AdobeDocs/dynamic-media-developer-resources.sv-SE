---
description: Svarets bildhöjd. Anger skalningen av den återgivna bilden så att höjden på svarsbilden inte är större än det angivna värdet, samtidigt som bildens proportioner behålls.
seo-description: Svarets bildhöjd. Anger skalningen av den återgivna bilden så att höjden på svarsbilden inte är större än det angivna värdet, samtidigt som bildens proportioner behålls.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# hei{#hei}

Svarets bildhöjd. Anger skalningen av den återgivna bilden så att höjden på svarsbilden inte är större än det angivna värdet, samtidigt som bildens proportioner behålls.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Svarets bildhöjd i pixlar (heltal större än 0). </p></td> 
 </tr> 
</table>

Bilden läggs inte till om både `wid=` och `hei=` har angetts och bredd/höjd skiljer sig från bildens proportioner.

`wid=` och  `hei=` arbeta tillsammans för att definiera storleken på bilden som returneras av servern. Om `scl=` kommer efter `wid=` eller `hei=` i URL:en avbryts dessa kommandon och `scl=` definierar storleken på bilden som returneras av servern.

Om `wid=` eller `hei=` kommer efter `scl=` i URL:en avbryts `scl=` och `wid=`/`hei=` för att definiera storleken på bilden som returneras av servern.

>[!NOTE]
>
>Ett fel returneras om den beräknade eller standardinställda svarsbildstorleken är större än `attribute::MaxPix`.

## Egenskaper {#section-6cbc6acd37c847beab84c896ac25280c}

Kan inträffa var som helst i begäran. Om du ändrar storlek på bilden med `wid=`, `hei=` eller `scl=` ändras inte utskriftsupplösningsvärdet som är inbäddat i svarsbilden. Ignoreras om `scl=` inträffar efter `wid=` och/eller `hei=` i kommandosekvensen.

## Standard {#section-61043f6c1f5d450883ff9e5eafd95955}

Om varken `wid=`, `hei=` eller `scl=` anges, skalas svarsbilden så att den passar i den storlek som definieras av `attribute::DefaultPix`. Om `attribute::DefaultPix` är tom har svarsbilden samma storlek som vinjettens visningsbild.

## Se även {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
