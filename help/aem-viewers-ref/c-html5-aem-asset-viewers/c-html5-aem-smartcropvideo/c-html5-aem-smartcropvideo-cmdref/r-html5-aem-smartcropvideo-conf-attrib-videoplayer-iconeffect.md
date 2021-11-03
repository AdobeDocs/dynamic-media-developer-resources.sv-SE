---
description: Konfigurationsattribut för visningsprogrammet för smart beskärning.
solution: Experience Manager
title: SmartCropVideoPlayer.iconeffect
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

Konfigurationsattribut för visningsprogrammet för smart beskärning.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`antal`*][, *`tona`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Gör att IconEffect kan visas ovanpå videon när videon pausas. På vissa enheter används inbyggda kontroller. I sådana fall <span class="codeph"> ikoneffekt</span> modifierare ignoreras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> antal</span> </span> </p> </td> 
   <td colname="col2"> <p> Anger det maximala antalet gånger som IconEffect visas och visas igen. Värdet för <span class="codeph"> -1</span> anger att ikonen visas oändligt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tona</span> </span> </p> </td> 
   <td colname="col2"> <p> Anger hur länge animeringen ska visas eller döljas, i sekunder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Anger antalet sekunder som IconEffect ska vara synlig innan den döljs automatiskt. Det vill säga, tiden efter att animeringen har tonats in är slutförd och innan animeringen börjar tonas ut. En inställning för <span class="codeph"> 0</span> inaktiverar beteende som döljer automatiskt. </p> </td> 
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
