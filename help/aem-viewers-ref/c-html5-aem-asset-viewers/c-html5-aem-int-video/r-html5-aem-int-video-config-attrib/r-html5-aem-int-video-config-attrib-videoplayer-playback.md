---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut för Interactive Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. </p> <p>När <span class="codeph"> auto</span> är inställt använder visningsprogrammet HTML5-direktuppspelad video i HLS-format i de flesta webbläsare och alla iOS-enheter och återgår till progressiv HTML5-uppspelning i vissa system som äldre Internet Explorer och Android. </p> <p>När <span class="codeph"> progressiv</span> är inställt förlitar sig visningsprogrammet endast på HTML5-uppspelning som stöds av webbläsare och spelar upp video progressivt på alla system. </p> <p>Mer information om hur du väljer uppspelning i inbyggda lägen för <span class="codeph"> auto</span> och <span class="codeph"> progressiva</span> finns i användarhandboken för HTML5-visningsprogram för SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
