---
description: Konfigurationsattribut för Video360 Viewer.
seo-description: Konfigurationsattribut för Video360 Viewer.
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# Video360Player.playback{#video-player-playback}

Konfigurationsattribut för Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. </p> <p>När <span class="codeph"> auto</span> är inställt använder visningsprogrammet HTML5-direktuppspelad video i HLS-format i de flesta webbläsare och alla iOS-enheter och återgår till progressiv HTML5-uppspelning i vissa system som äldre Internet Explorer och Android. </p> <p>När <span class="codeph"> progressiv</span> är inställt förlitar sig visningsprogrammet endast på HTML5-uppspelning som stöds av webbläsare och spelar upp video progressivt på alla system. </p> <p>Mer information om hur du väljer uppspelning i inbyggda lägen för <span class="codeph"> auto</span> och <span class="codeph"> progressiva</span> finns i användarhandboken för HTML5-visningsprogram för SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt. Ignoreras när visningsprogrammet fungerar med extern video.

Mer information finns i [Stöd för extern video](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760).

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
