---
description: Konfigurationsattribut för Video Viewer.
seo-description: Konfigurationsattribut för Video Viewer.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 5ab7a322-9de0-4a26-95be-b9b2ff8e5a84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut för Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. När <span class="codeph"> auto</span> är inställt används HTML5-direktuppspelad video i HLS-format i de flesta webbläsare och på alla iOS-enheter. Den återgår till progressiv HTML5-uppspelning på vissa system som äldre Internet Explorer och Android. </p> <p>Om du anger <span class="codeph"> progressiv</span> förlitar sig visningsprogrammet endast på HTML5-uppspelning, eftersom det stöds av webbläsare och video spelas upp progressivt på alla system. </p> <p>Mer information om hur du väljer uppspelning i automatiskt och progressivt läge finns i användarhandboken för Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

Ignoreras när visningsprogrammet fungerar med extern video. Se Stöd för [extern video](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

