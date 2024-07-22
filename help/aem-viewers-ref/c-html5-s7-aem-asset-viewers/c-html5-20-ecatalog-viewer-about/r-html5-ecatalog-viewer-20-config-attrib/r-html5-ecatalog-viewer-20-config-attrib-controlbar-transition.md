---
title: ControlBar.transition
description: Anger den effekttyp som används för att visa eller dölja kontrollfältet och dess innehåll.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona </span> </p> </td> 
   <td colname="col2"> <p> Anger den effekttyp som används för att visa eller dölja kontrollfältet och dess innehåll. Använd <span class="codeph"> ingen </span> för att visa och dölja omedelbart. <span class="codeph"> Tona </span> ger en gradvis in- och uttoningseffekt (stöds inte i Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder mellan den senaste mus-/beröringshändelsen som kontrollfältet registrerar och döljningen av tidskontrollfältet. </p> <p> Om den anges till <span class="codeph"> -1 </span> utlöser komponenten aldrig sin automatiska döljningseffekt och förblir alltid synlig på skärmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger längden på in- och uttoningsanimeringen, i sekunder. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt. Det här kommandot ignoreras på enheter med pekskärm, där det automatiska döljningsfältet är inaktiverat.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
