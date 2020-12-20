---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: cde4a5b9-4512-41a6-84ce-9f4fc2cc0399
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut för Interactive Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona</span> </p> </td> 
   <td colname="col2"> <p> Anger vilken effekttyp som ska användas för att visa/dölja kontrollfältet och dess innehåll. </p> <p>Ange <span class="codeph"> none</span> för direktvisning/dölj. </p> <p>Ange <span class="codeph"> tona</span> för att få en gradvis toningseffekt. Stöds inte i Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Anger tiden i sekunder mellan den senaste mus-/pekhändelsen som registrerats av kontrollfältet och tidskontrollfältet döljs. Om den anges till <span class="codeph"> -1</span> utlöser komponenten aldrig sin auto-hide-effekt och förblir därför alltid synlig på skärmen. </p> </td> 
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

