---
title: Video360Player.playback
description: Konfigurationsattribut för Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# Video360Player.playback{#video-player-playback}

Konfigurationsattribut för Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. </p> <p>När <span class="codeph"> auto</span> är inställt, i de flesta webbläsare och på alla iOS-enheter använder visningsprogrammet direktuppspelad HTML5-video i HLS-format. Dessutom återgår den till progressiv uppspelning i HTML5 i vissa system som äldre Internet Explorer och Android™. </p> <p>När <span class="codeph"> progressiv</span> är inställt förlitar sig visningsprogrammet endast på uppspelning i HTML5, eftersom det stöds av webbläsare och video spelas upp progressivt på alla system. </p> <p>Mer information om uppspelningsmarkeringen i <span class="codeph"> auto</span> och <span class="codeph"> progressiv</span> inbyggda lägen finns i användarhandboken för HTML5 Viewers SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt. Ignoreras när visningsprogrammet fungerar med extern video.

Se [Stöd för extern video](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) för mer information.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
