---
title: Ikoneffekt för videospelare
description: Ikonen Spela upp visas på videovisningsområdet. Den visas när videon pausas eller när slutet av videon nås, och den beror också på parametern iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Ikoneffekt för videospelare{#video-player-icon-effect}

Ikonen Spela upp visas på videovisningsområdet. Den visas när videon pausas eller när slutet av videon nås, och den beror också på parametern iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet på uppspelningsikonen styrs med följande CSS-klassväljare:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**CSS-egenskaper för uppspelningsikonen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Den bild som visas för uppspelningsikonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Uppspelningsikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Uppspelningsikonens höjd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ikoneffekten stöder attributväljaren `state`. Väljaren `state="play"` används när videon pausas mitt i uppspelningen och `state="replay"` används när spelhuvudet är i slutet av direktuppspelningen.

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Ställ in en 100 x 100 pixlar stor uppspelningsikon.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
