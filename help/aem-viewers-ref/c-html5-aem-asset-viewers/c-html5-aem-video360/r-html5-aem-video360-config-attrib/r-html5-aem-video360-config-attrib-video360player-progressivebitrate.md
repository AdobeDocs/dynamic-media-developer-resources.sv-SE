---
title: Video360Player.progressivebitrate
description: Konfigurationsattribut för Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 5%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Konfigurationsattribut för Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Anger önskad videobithastighet (i kilobit per sekund eller kbit/s) att spela upp från en adaptiv videouppsättning om det aktuella systemet inte har stöd för adaptiv videouppspelning. </p> <p>Komponenten hämtar videoströmmen med den högsta möjliga (men inte högre) bithastigheten till det angivna värdet. Om alla videoströmmar i den adaptiva videouppsättningen har högre kvalitet än det angivna värdet väljer logiken bithastigheten med den lägsta kvaliteten. </p> </td> 
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
