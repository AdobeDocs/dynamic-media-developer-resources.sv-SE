---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
   <td colname="col2"> <p>Anger den videobithastighet (i kilobit per sekund eller kbit/s) som används för den första videouppspelningen på stationära datorer. </p> <p>Om det här bithastighetsvärdet inte finns i den adaptiva videouppsättningen startar videospelaren den video som har den näst lägsta bithastigheten. </p> <p>Om inställt på <span class="codeph"> 0 </span>startar videospelaren från lägsta möjliga bithastighet. Gäller endast för system som inte har inbyggt stöd för HLS-video i HTML5 (som är webbläsarna Firefox, Chrome och Internet Explorer 11 i Windows 10) och när uppspelningsläget är inställt på <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
