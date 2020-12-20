---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 30f133bd-09c7-4d70-bcc4-d961bb028e55
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona  </span> </p> </td> 
   <td colname="col2"> <p> Anger den effekttyp som används för att visa eller dölja kontrollfältet och dess innehåll. Använd <span class="codeph"> ingen </span> för att omedelbart visa och dölja; <span class="codeph"> toning </span> ger en gradvis toning in- och uttoningseffekt (stöds inte i Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder mellan den senaste mus-/pekhändelsen som kontrollfältet registrerar och tidskontrollfältet döljs. </p> <p> Om den är inställd på <span class="codeph"> -1 </span> utlöser komponenten aldrig sin auto-hide-effekt och förblir alltid synlig på skärmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> varaktighet  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger längden på in- och uttoningsanimeringen i sekunder. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt. Det här kommandot ignoreras på enheter med pekskärm, där det automatiska döljningsfältet är inaktiverat.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
