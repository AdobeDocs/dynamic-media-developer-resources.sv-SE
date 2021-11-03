---
description: Konfigurationsattribut för visningsprogrammet för smart beskärning.
solution: Experience Manager
title: SmartCropVideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

Konfigurationsattribut för visningsprogrammet för smart beskärning.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Anger (i kbit per sekund eller kbit/s) den videobithastighet som ska spelas upp från en adaptiv videouppsättning om det aktuella systemet inte har stöd för adaptiv videouppspelning. </p> <p>Komponenten hämtar videoströmmen med den högsta möjliga bithastigheten (men inte högre) till det angivna värdet. Om alla videoströmmar i den adaptiva videouppsättningen har högre kvalitet än det angivna värdet väljer logiken bithastigheten med den lägsta kvaliteten. </p> </td> 
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
