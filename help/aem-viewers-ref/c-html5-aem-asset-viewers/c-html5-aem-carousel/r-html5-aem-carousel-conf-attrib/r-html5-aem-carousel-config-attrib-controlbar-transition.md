---
description: Konfigurationsattribut för Carousel Viewer.
seo-description: Konfigurationsattribut för Carousel Viewer.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut för Carousel Viewer.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona</span> </p> </td> 
   <td colname="col2"> <p> Anger den effekttyp som används för att visa eller dölja kontrollfältet och dess innehåll. </p> <p>Ange <span class="codeph"> none</span> för direktvisning/dölj. </p> <p>Ange <span class="codeph"> tona</span> för att få en gradvis toningseffekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder mellan den senaste mus-/pekhändelsen som registrerats av kontrollfältet och tidskontrollfältet döljs. </p> <p>Om den anges till <span class="codeph"> -1</span> utlöser komponenten aldrig sin auto-hide-effekt och förblir därför alltid synlig på skärmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> varaktighet</span></span> </p> </td> 
   <td colname="col2"> <p> Anger längden på in-/uttoningsanimeringen i sekunder. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt. Det här kommandot ignoreras på touchenheter där det automatiska döljningsfältet är inaktiverat.

## Standard {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

