---
description: Konfigurationsattribut för Video Viewer.
seo-description: Konfigurationsattribut för Video Viewer.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Konfigurationsattribut för Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Gör att IconEffect kan visas ovanpå videon när videon pausas. På vissa enheter används inbyggda kontroller. I så fall ignoreras <span class="codeph"> ikoneffektmodifieraren</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> antal</span></span> </p> </td> 
   <td colname="col2"> <p> Anger det maximala antalet gånger som IconEffect visas och visas igen. Värdet <span class="codeph"> -1</span> anger att ikonen visas oändligt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tona</span></span> </p> </td> 
   <td colname="col2"> <p> Anger hur länge animeringen ska visas eller döljas, i sekunder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Anger antalet sekunder som IconEffect ska vara synlig innan den döljs automatiskt. Det vill säga, tiden efter att animeringen har tonats in är slutförd och innan animeringen börjar tonas ut. Om du anger <span class="codeph"> 0</span> inaktiveras beteendet för att dölja automatiskt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```

