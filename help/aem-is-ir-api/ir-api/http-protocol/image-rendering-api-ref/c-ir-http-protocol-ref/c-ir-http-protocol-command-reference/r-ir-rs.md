---
description: Avancerade renderingsinställningar. Anger avancerade renderingsinställningar som ska användas vid rendering av den aktuella markeringen.
solution: Experience Manager
title: r
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# rs{#rs}

Avancerade renderingsinställningar. Anger avancerade renderingsinställningar som ska användas vid rendering av den aktuella markeringen.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Återgivningsinställningssträng. </p></td> 
 </tr> 
</table>

Används för finjustering av återgivningsutseende. Använd återgivningsfunktionen i utvecklingsverktyget (ingår i Dynamic Media Image Authoring package) för att skapa återgivningsinställningssträngar.

## Egenskaper {#section-9a2b2228789046658cb80eddf343af75}

Materialattribut.

## Standard {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Exempel {#section-47e4811882574441a4d517e42a35f352}

Efter lite experimenterande med bildredigering är det fastställt att USM (Unsharp-masking) ger rätt skärpa för det angivna programmet och materialet. Strängen för renderingsinställningar som konfigurerar USM kopieras till kommandot `rs=` som ska användas med det här materialet:

`…&rs=U2V20W50X2&…`

## Se även {#section-930116e735024a008c994547ba36ee40}

[katalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
