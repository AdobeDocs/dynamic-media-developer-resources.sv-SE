---
title: scl
description: Skalvyn. Skalar den återgivna bilden med den angivna skalningsfaktorn i förhållande till den helupplösta vinjetteringen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# scl{#scl}

Skalvyn. Skalar den återgivna bilden med den angivna skalningsfaktorn i förhållande till den helupplösta vinjetteringen.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>Inverterad skalfaktor (verklig, 1,0 eller högre). </p></td> 
 </tr> 
</table>

If `scl=` kommer efter `wid=` eller `hei=` i URL:en avbryts dessa kommandon och `scl=` definierar storleken på bilden som returneras av servern.

Om `wid=` eller `hei=` kommer efter `scl=` i URL:en avbryts de `scl=` och `wid=`/ `hei=` Definiera storleken på den bild som servern returnerar.

>[!NOTE]
>
>Ett fel returneras om den beräknade eller standardinställda svarsbilden är större än `attribute::MaxPix`.

## Egenskaper {#section-170458cbd6984bd59a3434431258b20f}

Kan inträffa var som helst i begäran. Ignoreras om `wid=` eller `hei=` inträffar efter `scl=` i kommandosekvensen.

Ändra storlek på bilden med `scl=` ändrar inte utskriftsupplösningsvärdet som är inbäddat i svarsbilden.

## Standard {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

If `wid=`, `hei=`, eller `scl=` har inte angetts, skalas svarsbilden så att den passar i den storlek som definieras av `attribute::DefaultPix`. If `attribute::DefaultPix` är tom har svarsbilden samma storlek som vinjettens visningsbild.

## Se även {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
