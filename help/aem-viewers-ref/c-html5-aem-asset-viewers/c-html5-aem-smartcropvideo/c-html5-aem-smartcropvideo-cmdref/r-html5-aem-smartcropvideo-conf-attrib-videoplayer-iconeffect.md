---
title: SmartCropVideoPlayer.iconeffect
description: Konfigurationsattribut för visningsprogrammet för smart beskärning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 369e389c-f0e2-405e-b4aa-2f6b9ac8b8ea
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

Konfigurationsattribut för visningsprogrammet för smart beskärning.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Gör att IconEffect kan visas ovanpå videon när videon pausas. På vissa enheter används inbyggda kontroller. I så fall ignoreras modifieraren <span class="codeph"> iconeffect </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger det maximala antalet gånger som IconEffect visas och visas igen. Värdet <span class="codeph"> -1</span> anger att ikonen visas oändligt igen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tona </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger hur länge animeringen ska visas eller döljas, i sekunder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
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
