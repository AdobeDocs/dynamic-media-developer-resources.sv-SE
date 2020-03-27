---
description: Konfigurationsattribut för Video Viewer.
seo-description: Konfigurationsattribut för Video Viewer.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: df669b2e-31da-4de0-b480-e54402c9545c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Konfigurationsattribut för Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span></span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av ett enda klick/tryck för att växla uppspelning/paus. Om du anger <span class="codeph"> Ingen</span> inaktiveras enkel musklickning/tryck för att spela upp/pausa. Om inställningen är <span class="codeph"> playPause</span>växlar klippet mellan att spela upp och pausa videon när du klickar på videon. På vissa enheter kan du använda inbyggda kontroller. I så fall <span class="codeph"> är funktionen för att klicka</span> en gång inaktiverad. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```

