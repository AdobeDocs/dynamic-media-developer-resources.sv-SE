---
description: Konfigurationsattribut för Video Viewer.
seo-description: Konfigurationsattribut för Video Viewer.
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: b2dde5f4-0449-4cad-a1f2-e336027f92c6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Konfigurationsattribut för Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value  </span> </p> </td> 
   <td colname="col2"> <p>Ställer in den videobithastighet i kbit/s eller kbit/s som används för den första videouppspelningen på stationära datorer. </p> <p>Om det här bithastighetsvärdet inte finns i den adaptiva videouppsättningen startar videospelaren den video som har den näst lägsta bithastigheten. </p> <p>Om <span class="codeph"> 0 </span> anges startar videospelaren från den lägsta möjliga bithastigheten. Gäller endast för system som inte har inbyggt stöd för HTML5 HLS-video (som är webbläsarna Firefox, Chrome och Internet Explorer 11 i Windows 10) och när uppspelningsläget är inställt på <span class="codeph"> auto </span>. </p> </td> 
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

