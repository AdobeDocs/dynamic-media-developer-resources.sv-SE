---
title: VideoPlayer.progressivebitrate
description: Konfigurationsattribut för Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Konfigurationsattribut för Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Anger önskad videobithastighet (i kilobit per sekund eller kbit/s) som ska spelas upp från en adaptiv videouppsättning om det aktuella systemet inte har stöd för adaptiv videouppspelning. </p> <p>Komponenten hämtar videoströmmen med den högsta möjliga bithastigheten (men inte högre) till det angivna värdet. Om alla videoströmmar i den adaptiva videouppsättningen har högre kvalitet än det angivna värdet väljer logiken bithastigheten med den lägsta kvaliteten. </p> </td> 
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
