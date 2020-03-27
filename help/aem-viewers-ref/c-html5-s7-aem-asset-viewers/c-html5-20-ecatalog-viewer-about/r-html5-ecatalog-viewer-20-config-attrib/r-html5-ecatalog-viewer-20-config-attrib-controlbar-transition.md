---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: e029173b-c004-4be8-b304-d6e2183314ad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona </span> </p> </td> 
   <td colname="col2"> <p> Anger den effekttyp som används för att visa eller dölja kontrollfältet och dess innehåll. Använd <span class="codeph"> ingen </span> för direktvisning och dölj; <span class="codeph"> toning </span> ger en gradvis toningseffekt (stöds inte i Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span></span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder mellan den senaste mus-/pekhändelsen som kontrollfältet registrerar och tidskontrollfältet döljs. </p> <p> Om värdet är <span class="codeph"> -1 utlöser </span> komponenten aldrig sin automatiska döljningseffekt och förblir alltid synlig på skärmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> varaktighet </span></span> </p> </td> 
   <td colname="col2"> <p> Anger längden på in- och uttoningsanimeringen i sekunder. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt. Det här kommandot ignoreras på enheter med pekskärm, där det automatiska döljningsfältet är inaktiverat.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
