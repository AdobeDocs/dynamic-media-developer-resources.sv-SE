---
description: Konfigurationsattribut för visningsprogrammet för blandad media.
seo-description: Konfigurationsattribut för visningsprogrammet för blandad media.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Mixa medieuppsättningar
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut för visningsprogrammet för blandad media.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. När <span class="codeph"> auto</span> är inställt använder visningsprogrammet HTML5-direktuppspelad video i HLS-format på de flesta webbläsare och alla iOS-enheter. Den återgår till progressiv HTML5-uppspelning på vissa system som äldre Internet Explorer och Android. </p> <p>Om <span class="codeph"> progressiv</span> har angetts förlitar sig visningsprogrammet bara på HTML5-uppspelning, eftersom det stöds av webbläsare och video spelas upp progressivt på alla system. </p> <p>Mer information om hur du väljer uppspelning i automatiskt och progressivt läge finns i användarhandboken för Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
