---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`tidsövergång`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tid</span></span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder som animeringen för en enskild zoomstegsåtgärd utförs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> övergång</span></span> </p> </td> 
   <td colname="col2"> <p> Skapar en illusion av acceleration eller retardation som gör att övergången ser mer naturlig ut. Du kan ange övergångar på något av följande sätt: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (automatiskt) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (linjär) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (kvadratiskt) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (kubik) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (kvartilt) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (kintic) </li> 
     </ul> </p> <p>I det automatiska läget används alltid linjär övergång när elastisk zoom är inaktiverat (standard). Annars passar den en av de andra övergångsfunktionerna baserat på övergångstiden. Det innebär att ju kortare övergångstiden är desto högre easing-funktion används för att accelerera hastigheten eller retardationseffekten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
