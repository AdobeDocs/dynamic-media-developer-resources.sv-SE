---
title: wid
description: Svarets bildbredd. Anger skalningen av den återgivna bilden så att svarsbilden inte är högre än det angivna värdet, samtidigt som bildens proportioner bevaras.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# wid{#wid}

Svarets bildbredd. Anger skalningen av den återgivna bilden så att svarsbilden inte är högre än det angivna värdet, samtidigt som bildens proportioner bevaras.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Bildbredd i pixlar (int större än 0). </p></td> 
 </tr> 
</table>

Bilden läggs inte till om båda `wid=` och `hei=` anges och `wid`/ `hei` skiljer sig från bildens proportioner.

`wid=` och `hei=` arbeta tillsammans för att definiera storleken på bilden som returneras av servern. If `scl=` kommer efter `wid=` eller `hei=` i URL:en avbryts dessa kommandon och `scl=` definierar storleken på bilden som returneras av servern.

Om `wid=` eller `hei=` kommer efter `scl=` i URL:en avbryts de `scl=` och `wid=`/ `hei=` Definiera storleken på den bild som servern returnerar.

>[!NOTE]
>
>Ett fel returneras om den beräknade eller standardinställda svarsbilden är större än `attribute::MaxPix`.

## Egenskaper {#section-2d067c6d371748e19cb157684700a49d}

Kan inträffa var som helst i begäran. Ändra storlek på bilden med `wid=`, `hei=`, eller `scl=` ändrar inte utskriftsupplösningsvärdet som är inbäddat i svarsbilden. Ignoreras om `scl=` inträffar efter `wid=` eller `hei=` i kommandosekvensen.

## Standard {#section-c7c6efa03d864592a3398b6f1de5a0b0}

If `wid=`, `hei=`, eller `scl=` har inte angetts, skalas svarsbilden så att den passar i den storlek som definieras av `attribute::DefaultPix`. If `attribute::DefaultPix` är tom har svarsbilden samma storlek som vinjettens visningsbild.

## Se även {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
