---
title: groda
description: Färg och tjocklek på plattans skala. Simulerar murbruk för keramiska och naturliga stenplattor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# groda {#grout}

Färg och tjocklek på plattans skala. Simulerar murbruk för keramiska och naturliga stenplattor.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> färg </span> </span> </p> </td>
  <td class="stentry"> <p>Groutfärg (grå eller RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>Grovtjocklek. scenkoordinatenheter (vanligtvis tum) (verkliga). </p> </td>
 </tr> 
</table>

För maximal kontroll av jordningens utseende gäller följande krav:

* Plattan ska vara kvadratisk eller rektangulär. inga andra former stöds för närvarande.
* Bilden får endast innehålla en platta.
* Standardutfallet i bilden (om sådan finns) måste ha samma tjocklek på alla fyra kanterna.
* Standardjordningens tjocklek måste anges i materialkatalogen ( `catalog::GroutWidth`).

## Egenskaper {#section-de78b678245b4ffda48097c345949e77}

Materialattribut. `*`färg`*` Måste vara ett RGB-färgvärde. `*`width`*` måste vara ett reellt värde 0 eller större.

Ignoreras om upprepning = 4, 5, 7, 8, 9, 14 eller högre, eller om detta anges för andra material än repeterbara texturer.

## Standard {#section-bfab3621f70b4489a21994ab11b20cc6}

If `grout=` anges inte, bildens gruppering ändras inte. If `grout= *`färg`*` anges, `*`width`*` standardvärdet är `catalog::GroutWidth`.

## Se även {#section-8d472906a44943f5a8557e98f2fbc71f}

[Färgvärden](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
