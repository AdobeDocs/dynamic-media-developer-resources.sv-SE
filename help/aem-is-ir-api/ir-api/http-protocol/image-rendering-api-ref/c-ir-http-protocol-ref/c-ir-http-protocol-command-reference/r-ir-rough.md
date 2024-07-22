---
title: grov
description: Materialytans grovhet. Anger materialytans relativa grovhet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# grov{#rough}

Materialytans grovhet. Anger materialytans relativa grovhet.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Ytojämnhet (0...100 procent) eller -1 för att välja standardgrovhet. </p> </td> 
 </tr> 
</table>

Används för att styra återgivningseffekten för 3D-reflektion. Lägre värden för grovhet ger vanligen jämnare reflektionseffekter och högre värden ger slumpgenerering och spridning av den reflekterade bilden.

Varje materialtyp ( `type=`) definierar en minimal och maximal reflektionsåtergivningseffekt baserat på grovhet. För vissa materialtyper (till exempel väggpapper) har `rough=` minimal inverkan på reflektionens utseende, medan effekten är betydligt mer uttalad för andra materialtyper (till exempel sten eller keramik).

`rough=-1` Anger grovheten till ett serverinternt standardvärde (40 % för vanliga materialtyper).

## Egenskaper {#section-515375758b254c80af576271bdb61bb8}

Materialattribut. Ignoreras om vinjetteringen inte har någon 3D-reflektionskapacitet, om målobjektet inte har någon 3D-geometri associerad med den eller om målobjektet inte reflekterar några andra objekt i scenen.

## Standard {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` Om materialet baseras på en katalogpost, annars ungefär 40 %.

## Se även {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
