---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Konfigurationsattribut för Interactive Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Anger den videobithastighet (i kbit/s eller kbit/s) som används för den första videouppspelningen på en dator. </p> <p>Om det här bithastighetsvärdet inte finns i den adaptiva videouppsättningen startar videospelaren med videon som har den näst lägre bithastigheten. </p> <p>Om <span class="codeph"> 0</span> anges startar videospelaren från den lägsta möjliga bithastigheten. </p> <p>Gäller endast för system som inte har inbyggt stöd för HTML5 HLS-video (till exempel webbläsarna Firefox, Chrome och Internet Explorer 11 i Windows 10) och när uppspelningsläget är inställt på auto. </p> </td> 
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
