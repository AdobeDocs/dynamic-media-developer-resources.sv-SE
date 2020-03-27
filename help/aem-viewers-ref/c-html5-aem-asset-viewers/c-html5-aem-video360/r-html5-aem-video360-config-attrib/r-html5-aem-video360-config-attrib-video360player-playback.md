---
description: Konfigurationsattribut för Video360 Viewer.
seo-description: Konfigurationsattribut för Video360 Viewer.
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
topic: Dynamic media
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.playback{#video-player-playback}

Konfigurationsattribut för Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Anger den typ av uppspelning som används av visningsprogrammet. </p> <p>När <span class="codeph"> auto</span> är inställt används HTML5-direktuppspelad video i HLS-format i de flesta webbläsare och på alla iOS-enheter, och HTML5-uppspelningen återgår till progressiv HTML5-uppspelning i vissa system som äldre Internet Explorer och Android. </p> <p>När <span class="codeph"> progressiv</span> är inställt förlitar sig visningsprogrammet endast på HTML5-uppspelning eftersom det stöds av webbläsare och video spelas upp progressivt på alla system. </p> <p>Mer information om hur du väljer uppspelning i <span class="codeph"> automatiskt</span> och <span class="codeph"> progressivt</span> inbyggt läge finns i användarhandboken för HTML5-visningsprogram för SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt. Ignoreras när visningsprogrammet fungerar med extern video.

Mer information finns i Stöd [för](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) extern video.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
