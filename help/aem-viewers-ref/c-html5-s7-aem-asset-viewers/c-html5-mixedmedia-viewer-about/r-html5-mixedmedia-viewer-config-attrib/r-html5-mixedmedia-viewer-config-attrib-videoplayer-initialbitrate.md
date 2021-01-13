---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>Ställer in den videobithastighet i kbit/s eller kbit/s som används för den första videouppspelningen på stationära datorer. </p> <p>Om det här bithastighetsvärdet inte finns i den adaptiva videouppsättningen startar videospelaren den video som har den näst lägsta bithastigheten. </p> <p>Om <span class="codeph"> 0 </span> anges startar videospelaren från den lägsta möjliga bithastigheten. Gäller endast för system som inte har inbyggt stöd för HTML5 HLS-video (som är webbläsarna Firefox, Chrome och Internet Explorer 11 i Windows 10) och när uppspelningsläget är inställt på <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
