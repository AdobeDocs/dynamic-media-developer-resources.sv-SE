---
description: 'null'
seo-description: 'null'
seo-title: PageView.transition
solution: Experience Manager
title: PageView.transition
topic: Dynamic media
uuid: c85ad85f-a802-4f5d-9046-00171ad2d9ca
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.transition{#pageview-transition}

[!DNL `[PageView.|<containerId>_pageView.]transition= *``*[, *`tidsövergång`*]`]

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tid</span></span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder som animeringen för en enskild zoomstegsåtgärd utförs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> övergång</span></span> </p> </td> 
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

## Egenskaper {#section-ebfd9162c8504666bf0e4485bf3b1383}

Valfritt.

## Standard {#section-9f91ce6567384ab691e4d4f8a7015455}

[!DNL `0.5,0`]

## Exempel {#section-cb6b8793ee9946b8bf1cfddab8612db5}

[!DNL `transition=2,2`]
