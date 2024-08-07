---
title: VideoPlayer.progressivebitrate
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Konfigurationsattribut för Interactive Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`värde`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> värde </span> </p> </td> 
   <td colname="col2"> <p> Anger önskad videobithastighet som ska spelas upp från en adaptiv videouppsättning i kilobit per sekund (kbit/s) om det aktuella systemet inte har stöd för adaptiv videouppspelning. </p> <p>Komponenten hämtar videoströmmen med den högsta möjliga (men inte högre) bithastigheten till det angivna värdet. Om alla videoströmmar i den adaptiva videouppsättningen har högre kvalitet än det angivna värdet väljer logiken bithastigheten med den lägsta kvaliteten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
