---
description: Konfigurationsattribut för Video Viewer.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Video
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Konfigurationsattribut för Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av ett enda klick/tryck för att växla uppspelning/paus. Om du anger <span class="codeph"> none</span> inaktiveras enkelklickning/tryck för att spela upp/pausa. Om värdet är <span class="codeph"> playPause</span> växlar videon mellan att spela upp och pausa videon när du klickar på den. På vissa enheter kan du använda inbyggda kontroller. I så fall är <span class="codeph">-beteendet </span> inaktiverat. </p> </td> 
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

