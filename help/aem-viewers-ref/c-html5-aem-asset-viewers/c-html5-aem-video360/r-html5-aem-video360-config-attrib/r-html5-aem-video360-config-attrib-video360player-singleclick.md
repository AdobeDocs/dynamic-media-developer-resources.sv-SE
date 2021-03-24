---
description: Konfigurationsattribut för Video360 Viewer.
solution: Experience Manager
title: Video360Player.singleclick
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---


# Video360Player.singleclick{#video-player-singleclick}

Konfigurationsattribut för Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

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

