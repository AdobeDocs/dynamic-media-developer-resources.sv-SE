---
description: Uppspelningsikonen visas i huvudvisningsområdet. Den visas när videon pausas eller när slutet av videon nås, och den beror också på parametern iconeffect.
seo-description: Uppspelningsikonen visas i huvudvisningsområdet. Den visas när videon pausas eller när slutet av videon nås, och den beror också på parametern iconeffect.
seo-title: Ikoneffekt
solution: Experience Manager
title: Ikoneffekt
topic: Dynamic media
uuid: dcab487d-0bd6-4899-82e2-e29fa812a864
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Ikoneffekt{#icon-effect}

Uppspelningsikonen visas i huvudvisningsområdet. Den visas när videon pausas eller när slutet av videon nås, och den beror också på parametern iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet på uppspelningsikonen styrs med följande CSS-klassväljare:

```
.s7videoviewer . s7videoplayer .s7iconeffect
```

**CSS-egenskaper för uppspelningsikonen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Den bild som visas för uppspelningsikonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Uppspelningsikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Uppspelningsikonens höjd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ikoneffekten stöder attributväljaren `state`. `state="play"` används när videon pausas mitt i uppspelningen och  `state="replay"` används när spelhuvudet är i slutet av direktuppspelningen.

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Ställ in en 100 x 100 pixlar uppspelningsikon.

```
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

