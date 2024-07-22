---
title: scl
description: Skalvyn. Skalar den sammansatta bilden med inverterad invFactor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# scl{#scl}

Skalvyn. Skalar den sammansatta bilden med inverterad invFactor.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor </span> </p> </td> 
  <td class="stentry"> <p>Inverterad skalfaktor (verklig större än 0,0). </p></td> 
 </tr> 
</table>

Ingen skalförändring används när `scl=1`. Ett *`invFactor`*-värde som är större än 1,0 nedskalningar och mindre än 1,0 förstorar den sammansatta bilden.

Om `scl=` anges och `wid=` och/eller `hei=` också finns, beskärs bilden till `wid=` och/eller `hei=` efter skalning.

>[!NOTE]
>
>Ett fel returneras om den beräknade eller standardinställda svarsbildstorleken är större än `attribute::MaxPix`.

## Egenskaper {#section-60af012719db477db4a4703e9a6da5f5}

Visa attribut. Det används oavsett den aktuella lagerinställningen.

## Standard {#section-32502fa218a24e1f9c65f41c0260b56a}

Om varken `wid=`, `hei=` eller `scl=` anges har svarsbilden antingen samma storlek som den sammansatta bilden eller `attribute::DefaultPix`, beroende på vilken som är minst.

## Exempel {#section-a33f6239476a4b438d939656ad99aa76}

Se exemplet i [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) för ett vanligt program i `scl=`.

## Se även {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
