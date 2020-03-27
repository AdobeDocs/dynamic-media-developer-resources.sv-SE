---
description: Materialytans grovhet. Anger materialytans relativa grovhet.
seo-description: Materialytans grovhet. Anger materialytans relativa grovhet.
seo-title: grov
solution: Experience Manager
title: grov
topic: Scene7 Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Används för att styra återgivningseffekten för 3D-reflektion. Lägre värden för grovhet ger vanligen jämnare reflektionseffekter. högre värden orsakar slumpgenerering och spridning av den reflekterade bilden.

Varje materialtyp ( `type=`) definierar en minimal och maximal reflektionseffekt som baseras på grovhet. För vissa materialtyper (t.ex. väggpapper) har `rough=` knappt någon inverkan på reflektionens utseende, medan effekten för andra materialtyper (t.ex. sten eller keramik) är betydligt mer uttalad.

`rough=-1` ställer in grovheten till ett serverinternt standardvärde (40 % för vanliga materialtyper).

## Egenskaper {#section-515375758b254c80af576271bdb61bb8}

Materialattribut. Ignoreras om vinjetteringen inte har någon 3D-reflektionskapacitet, om målobjektet inte har någon 3D-geometri associerad med den eller om målobjektet inte reflekterar några andra objekt i scenen.

## Standard {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` om materialet är baserat på en katalogpost, i annat fall ungefär 40 %.

## Se även {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
