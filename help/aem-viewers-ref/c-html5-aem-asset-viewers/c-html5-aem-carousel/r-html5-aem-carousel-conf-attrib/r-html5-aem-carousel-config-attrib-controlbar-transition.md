---
title: ControlBar.transition
description: Konfigurationsattribut för Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut för Carousel Viewer.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona</span> </p> </td> 
   <td colname="col2"> <p> Anger den effekttyp som används för att visa eller dölja kontrollfältet och dess innehåll. </p> <p>Ange <span class="codeph"> ingen</span> för direktvisning/dölj. </p> <p>Ange som <span class="codeph"> tonad</span> för att få en gradvis toningseffekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder mellan den senaste mus-/pekhändelsen som registrerats av kontrollfältet och tidskontrollfältet döljs. </p> <p>Om värdet är <span class="codeph"> -1</span> utlöser komponenten aldrig sin automatiska döljningseffekt och förblir därför alltid synlig på skärmen. </p> </td> 
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
