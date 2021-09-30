---
title: VideoPlayer.singleclick
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Konfigurationsattribut för Interactive Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av ett enda klick/tryck för att växla uppspelning/paus. Om du anger <span class="codeph"> none</span> inaktiveras enkelklickning/tryck för att spela upp/pausa. Om <span class="codeph"> playPause</span> är inställt på  växlar videon mellan att spela upp och pausa videon. På vissa enheter kan du använda inbyggda kontroller. I det här fallet är ett <span class="codeph">-beteende som innebär att användaren klickar på</span> inaktiverat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
