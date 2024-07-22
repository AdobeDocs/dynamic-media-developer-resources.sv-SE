---
title: ControlBar.transition
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut för Interactive Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona</span> </p> </td> 
   <td colname="col2"> <p> Anger den effekttyp som används för att visa/dölja kontrollfältet och dess innehåll. </p> <p>Ange <span class="codeph"> ingen</span> för direktvisning/dölj. </p> <p>Ange som <span class="codeph"> tonad</span> för att få en gradvis toningseffekt. Stöds inte i Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder mellan den senaste mus-/pekhändelsen som registrerats av kontrollfältet och tidskontrollfältet döljs. Om värdet är <span class="codeph"> -1</span> utlöser komponenten aldrig sin automatiska döljningseffekt och förblir därför alltid synlig på skärmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> varaktighet</span></span> </p> </td> 
   <td colname="col2"> <p> Anger längden på in-/uttoningsanimeringen i sekunder. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
