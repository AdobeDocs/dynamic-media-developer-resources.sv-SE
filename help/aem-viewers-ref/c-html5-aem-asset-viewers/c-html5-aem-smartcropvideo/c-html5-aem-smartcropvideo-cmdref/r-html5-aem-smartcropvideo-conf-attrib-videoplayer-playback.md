---
description: Konfigurationsattribut för visningsprogrammet för smart beskärning.
solution: Experience Manager
title: SmartCropVideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Konfigurationsattribut för visningsprogrammet för smart beskärning.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. När <span class="codeph"> auto</span> är inställt, i de flesta webbläsare och på alla iOS-enheter använder visningsprogrammet direktuppspelad HTML5-video i HLS-format. Den återgår till progressiv uppspelning i HTML5 på vissa system som äldre Internet Explorer och Android. </p> <p>If <span class="codeph"> progressiv</span> anges att visningsprogrammet endast förlitar sig på uppspelning i HTML5 eftersom det stöds av webbläsare och att videon spelas upp progressivt på alla system. </p> <p>Mer information om hur du väljer uppspelning i automatiskt och progressivt läge finns i användarhandboken för Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

Ignoreras när visningsprogrammet fungerar med extern video. Se [Stöd för extern video]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
