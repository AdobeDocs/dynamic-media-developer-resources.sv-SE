---
description: Konfigurationsattribut för Video360 Viewer.
solution: Experience Manager
title: Video360Player.initialbitrate
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Konfigurationsattribut för Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

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
