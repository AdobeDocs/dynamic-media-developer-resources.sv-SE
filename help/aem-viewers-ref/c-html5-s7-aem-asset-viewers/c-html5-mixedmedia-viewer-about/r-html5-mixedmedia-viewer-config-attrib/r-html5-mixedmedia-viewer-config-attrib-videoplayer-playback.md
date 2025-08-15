---
title: VideoPlayer.playback
description: Konfigurationsattribut för visningsprogrammet för blandad media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut för visningsprogrammet för blandad media.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. När <span class="codeph"> auto</span> har angetts används HTML5-direktuppspelad video i HLS-format i de flesta webbläsare och på alla iOS-enheter. Den återgår till progressiv uppspelning av HTML5 i vissa system som äldre Internet Explorer och Android™. </p> <p>Om <span class="codeph"> progressiv</span> har angetts förlitar sig visningsprogrammet bara på HTML5-uppspelning eftersom det stöds av webbläsare och video spelas upp progressivt på alla system. </p> <p>Mer information om hur du väljer uppspelning i automatiskt och progressivt läge finns i användarhandboken för Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
