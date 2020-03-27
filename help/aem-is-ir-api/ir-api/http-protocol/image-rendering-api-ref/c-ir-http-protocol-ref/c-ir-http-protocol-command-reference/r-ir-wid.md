---
description: Svarets bildbredd. Anger skalningen av den återgivna bilden så att svarsbilden inte är högre än det angivna värdet, samtidigt som bildens proportioner bevaras.
seo-description: Svarets bildbredd. Anger skalningen av den återgivna bilden så att svarsbilden inte är högre än det angivna värdet, samtidigt som bildens proportioner bevaras.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Bilden utfylls inte om både `wid=` och `hei=` anges och `wid`/ `hei` skiljer sig från bildens proportioner.

`wid=` och `hei=` arbeta tillsammans för att definiera storleken på bilden som returneras av servern. Om `scl=` kommer efter `wid=` eller `hei=` i URL:en avbryts dessa kommandon och storleken på bilden som returneras av servern `scl=` definieras.

Om `wid=` eller `hei=` kommer efter `scl=` i URL:en avbryts `scl=` och `wid=`/ `hei=` definierar de bildstorleken som returneras av servern.

>[!NOTE]
>
>Ett fel returneras om den beräknade eller standardinställda svarsbilden är större än `attribute::MaxPix`.

## Egenskaper {#section-2d067c6d371748e19cb157684700a49d}

Kan inträffa var som helst i begäran. Om du ändrar storlek på bilden med `wid=`, `hei=`eller `scl=` inte ändras värdet för utskriftsupplösning som är inbäddat i svarsbilden. Ignoreras om `scl=` inträffar efter `wid=` eller `hei=` i kommandosekvensen.

## Standard {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Om varken `wid=`, `hei=`eller `scl=` anges, skalas svarsbilden så att den passar i den storlek som definieras av `attribute::DefaultPix`. Om `attribute::DefaultPix` är tom får svarsbilden samma storlek som vinjettens visningsbild.

## Se även {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
