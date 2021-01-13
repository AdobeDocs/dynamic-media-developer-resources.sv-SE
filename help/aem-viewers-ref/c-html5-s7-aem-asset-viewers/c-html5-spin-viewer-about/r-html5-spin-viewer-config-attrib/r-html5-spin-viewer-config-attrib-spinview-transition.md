---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
topic: Dynamic media
uuid: 9d7ea421-9892-4276-8f22-3e1099f91f2f
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`tidsövergång`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tid</span></span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder som animeringen för en enskild zoomstegsåtgärd utförs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> övergång</span></span> </p> </td> 
   <td colname="col2"> <p> Skapar en illusion av acceleration eller retardation som gör att övergången ser mer naturlig ut. Du kan ange övergångar på något av följande sätt: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automatiskt) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linjär) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (kvadratiskt) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (kubik) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (kvartilt) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (kintic) </li> 
     </ul> </p> <p>I det automatiska läget används alltid linjär övergång när elastisk zoom är inaktiverat (standard). Annars passar den en av de andra övergångsfunktionerna baserat på övergångstiden. Det innebär att ju kortare övergångstiden är desto högre easing-funktion används för att accelerera hastigheten eller retardationseffekten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2`
