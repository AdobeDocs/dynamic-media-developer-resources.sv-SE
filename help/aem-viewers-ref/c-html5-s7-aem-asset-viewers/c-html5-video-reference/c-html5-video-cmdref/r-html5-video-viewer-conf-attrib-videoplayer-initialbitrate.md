---
title: VideoPlayer.initialbitrate
description: Konfigurationsattribut för Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Konfigurationsattribut för Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Anger den videobithastighet (i kilobit per sekund eller kbit/s) som används för den första videouppspelningen på stationära datorer. </p> <p>Om det här bithastighetsvärdet inte finns i den adaptiva videouppsättningen startar videospelaren den video som har den näst lägsta bithastigheten. </p> <p>Om inställt på <span class="codeph"> 0 </span>startar videospelaren från lägsta möjliga bithastighet. Gäller endast för system som inte har inbyggt stöd för HLS-video i HTML5 (som är webbläsarna Firefox, Chrome och Internet Explorer 11 i Windows 10) och när uppspelningsläget är inställt på <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
