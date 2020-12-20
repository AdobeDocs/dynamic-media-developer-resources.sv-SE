---
description: Bildschemadata. Innehåller data för bildschema för det här lagret. Åsidosätter alla data från katalogkartan för det här lagret.
seo-description: Bildschemadata. Innehåller data för bildschema för det här lagret. Åsidosätter alla data från katalogkartan för det här lagret.
seo-title: map
solution: Experience Manager
title: map
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---


# map{#map}

Bildschemadata. Innehåller data för bildschema för det här lagret. Åsidosätter alla data från katalogen::Map för det här lagret.

`map=[ *``*]mapA=[ *`stringstringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Bildschemadata för det här lagret i lagerkoordinater. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Bildschemadata för det här lagret i källbildens koordinater. </p></td> 
 </tr> 
</table>

En tom sträng anger att det här lagret inte ska innehålla ett bildschema. Strängen måste vara korrekt HTTP-kodad för att undvika tolkningsproblem.

Alla et-tecken (&amp;) i *`string`* måste vara http-kodade.

När `mapA=` och `catalog::Map` anger mappningsdata i källbildens koordinater, antar `map=` lagerkoordinaterna i förhållande till det övre, vänstra hörnet i lagerektangeln (efter att `rotate=` och `extend=` har tillämpats).

Bildschemat för utdata beskärs alltid till lagrets rektangel. Om attributet `shape` utelämnas eller är inställt på `default` används hela lagrets rektangel som bildschemaområde.

## Egenskaper {#section-a18d9ea95c71414a905a68b8839c0843}

Lagerattribut. När det används på `layer=comp`, lagras angivna schemadata bakom alla andra bildscheman. Ignorerad såvida inte `req=map`. Ignoreras av effektlager. `mapA=` ignoreras om  `map=` också anges.

## Standard {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` används om  `map=` inte anges.

## Exempel {#section-cd7691c94f984222845c86dcb0051ce8}

Definiera ett rektangulärt bildschema för ett enkelt textlager:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Ett `AREA`-element med (oftast) standardattribut används för att infoga kartområdet för hela lagrets rektangel.

## Se även {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Bildscheman](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab),  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
