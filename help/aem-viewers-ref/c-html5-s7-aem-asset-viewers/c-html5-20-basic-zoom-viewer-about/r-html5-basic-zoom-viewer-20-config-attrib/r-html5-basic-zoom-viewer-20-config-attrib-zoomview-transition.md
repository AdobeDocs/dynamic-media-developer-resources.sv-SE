---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3ae12e0a-0647-4cb1-9785-c854b4586c47
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`tid`*[, *`övergång`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> time </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder som animeringen för en enskild zoomstegsåtgärd utförs. </p> </td> 
  </tr>
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> övergång </span> </span> </p> </td> 
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

## Egenskaper {#section-50bcd15223174bb79ce08b31ea03d682}

Valfritt.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`0.5,0`

## Exempel {#section-96e69b70365f461dae4399e49044ea2f}

`transition=2,2`
