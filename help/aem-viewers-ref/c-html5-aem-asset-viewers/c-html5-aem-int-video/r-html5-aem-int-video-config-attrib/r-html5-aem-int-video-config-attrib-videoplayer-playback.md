---
title: VideoPlayer.playback
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut för Interactive Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. </p> <p>När <span class="codeph"> auto</span> är inställt, i de flesta webbläsare och på alla iOS-enheter använder visningsprogrammet direktuppspelad HTML5-video i HLS-format. Dessutom återgår den till progressiv uppspelning i HTML5 i vissa system som äldre Internet Explorer och Android™. </p> <p>När <span class="codeph"> progressiv</span> är inställt förlitar sig visningsprogrammet endast på uppspelning i HTML5, eftersom det stöds av webbläsare och video spelas upp progressivt på alla system. </p> <p>Mer information om uppspelningsmarkeringen i <span class="codeph"> auto</span> och <span class="codeph"> progressiv</span> inbyggda lägen finns i användarhandboken för HTML5 Viewers SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
