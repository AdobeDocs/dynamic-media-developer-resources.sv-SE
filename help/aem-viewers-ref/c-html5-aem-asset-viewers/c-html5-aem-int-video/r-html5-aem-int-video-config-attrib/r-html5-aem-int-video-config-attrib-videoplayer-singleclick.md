---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 1%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Konfigurationsattribut för Interactive Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av ett enda klick/tryck för att växla uppspelning/paus. Om du anger <span class="codeph"> none</span> inaktiveras enkelklickning/tryck för att spela upp/pausa. Om värdet är <span class="codeph"> playPause</span> växlar klippet mellan att spela upp och pausa videon när du klickar på videon. På vissa enheter kan du använda inbyggda kontroller. I det här fallet är ett <span class="codeph">-beteende som innebär att användaren klickar på</span> inaktiverat. </p> </td> 
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
