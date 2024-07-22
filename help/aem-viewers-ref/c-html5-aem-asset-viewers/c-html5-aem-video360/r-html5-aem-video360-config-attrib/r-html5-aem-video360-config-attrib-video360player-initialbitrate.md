---
title: Video360Player.initialbitrate
description: Konfigurationsattribut för Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Konfigurationsattribut för Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`värde`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> värde </span> </p> </td> 
   <td colname="col2"> <p> Anger den videobithastighet (i kilobit per sekund eller kbit/s) som används för den första videouppspelningen på en stationär dator. </p> <p>Om det här bithastighetsvärdet inte finns i den adaptiva videouppsättningen startar videospelaren med videon som har den näst lägre bithastigheten. </p> <p>Om värdet är <span class="codeph"> 0</span> startar videospelaren från lägsta möjliga bithastighet. </p> <p>Gäller endast för system som inte har inbyggt stöd för HLS-video i HTML5 (till exempel Firefox, Chrome och Internet Explorer 11-webbläsare i Windows 10) och när uppspelningsläget är inställt på auto. </p> </td> 
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
