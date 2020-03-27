---
description: Konfigurationsattribut för Video Viewer.
seo-description: Konfigurationsattribut för Video Viewer.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: abd98898-d7d8-468f-b696-052e61e171b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut för Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|tona</span> </p> </td> 
   <td colname="col2"> <p> Anger den effekttyp som används för att visa eller dölja kontrollfältet och dess innehåll. </p> <p>Använd <span class="codeph"> ingen</span> för direktvisning och dölj. Använd <span class="codeph"> toning</span> för att få en gradvis toningseffekt och toningseffekt. </p> <p>Tona stöds inte i Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p>Anger tiden i sekunder mellan den senaste mus-/pekhändelsen som kontrollfältet registrerar och tidskontrollfältet döljs. </p> <p> Om den är inställd på <span class="codeph"> -1</span> utlöser komponenten aldrig sin auto-hide-effekt och förblir alltid synlig på skärmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> varaktighet</span></span> </p> </td> 
   <td colname="col2"> <p>Anger längden på in- och uttoningsanimeringen i sekunder. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```

