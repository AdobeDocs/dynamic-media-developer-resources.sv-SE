---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 72438e50-29fc-484f-8a3b-be8909e7864f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Konfigurationsattribut för Interactive Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Anger önskad videobithastighet som ska spelas upp från en adaptiv videouppsättning i kbit/s (eller kbit/s) om det aktuella systemet inte har stöd för adaptiv videouppspelning. </p> <p>Komponenten hämtar videoströmmen med den högsta möjliga (men inte högre) bithastigheten till det angivna värdet. Om alla videoströmmar i den adaptiva videouppsättningen har högre kvalitet än det angivna värdet väljer logiken bithastigheten med den lägsta kvaliteten. </p> </td> 
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

