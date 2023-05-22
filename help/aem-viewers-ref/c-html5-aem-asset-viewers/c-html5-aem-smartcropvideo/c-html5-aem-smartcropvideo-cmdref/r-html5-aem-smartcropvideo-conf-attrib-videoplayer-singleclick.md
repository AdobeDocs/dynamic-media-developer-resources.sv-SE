---
title: SmartCropVideoPlayer.singleclick
description: Konfigurationsattribut för visningsprogrammet för smart beskärning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

Konfigurationsattribut för visningsprogrammet för smart beskärning.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av ett enda klick/tryck för att växla uppspelning/paus. Inställning till <span class="codeph"> ingen</span> inaktiverar enkelklickning/tryck för att spela upp/pausa. Om inställt på <span class="codeph"> playPause</span>, klickar du på videon för att växla mellan att spela upp och pausa videon. På vissa enheter kan du använda inbyggda kontroller. I sådana fall <span class="codeph"> singleclick</span> beteendet är inaktiverat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
