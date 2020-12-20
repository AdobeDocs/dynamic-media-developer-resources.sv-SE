---
description: Färg och tjocklek på plattans skala. Simulerar murbruk för keramiska och naturliga stenplattor.
seo-description: Färg och tjocklek på plattans skala. Simulerar murbruk för keramiska och naturliga stenplattor.
seo-title: groda
solution: Experience Manager
title: groda
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# grout{#grout}

Färg och tjocklek på plattans skala. Simulerar murbruk för keramiska och naturliga stenplattor.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> färg  </span> </span> </p> </td> 
  <td class="stentry"> <p>Groutfärg (grå eller RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width  </span> </span> </p> </td> 
  <td class="stentry"> <p>Grovtjocklek. scenkoordinatenheter (vanligtvis tum) (verkliga). </p> </td> 
 </tr> 
</table>

För maximal kontroll av jordningens utseende gäller följande krav:

* Plattan ska vara kvadratisk eller rektangulär. inga andra former stöds för närvarande.
* Bilden får endast innehålla en platta.
* Den förinställda utsöndringen i bilden (om sådan finns) måste ha exakt samma tjocklek på alla fyra kanterna.
* Tjockleken på standardutsnittet måste anges i materialkatalogen ( `catalog::GroutWidth`).

## Egenskaper {#section-de78b678245b4ffda48097c345949e77}

Materialattribut. ` *`Färgen `*` måste vara ett RGB-färgvärde. ` *`Bredden `*` måste vara ett reellt värde på 0 eller större.

Ignoreras om upprepning = 4, 5, 7, 8, 9, 14 eller högre, eller om detta anges för andra material än repeterbara texturer.

## Standard {#section-bfab3621f70b4489a21994ab11b20cc6}

Om `grout=` inte anges ändras inte bildens groout. Om ` grout= *`color`*` anges är ` *`width`*` som standard `catalog::GroutWidth`.

## Se även {#section-8d472906a44943f5a8557e98f2fbc71f}

[Färgvärden](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
