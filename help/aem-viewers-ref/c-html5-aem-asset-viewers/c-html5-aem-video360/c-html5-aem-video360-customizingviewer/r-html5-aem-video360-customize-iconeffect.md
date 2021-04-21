---
description: Uppspelningsikonen visas i huvudvisningsområdet. Den visas när videon pausas eller när slutet av videon nås, och den beror också på parametern iconeffect.
solution: Experience Manager
title: Ikoneffekt
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Ikoneffekt{#icon-effect}

Uppspelningsikonen visas i huvudvisningsområdet. Den visas när videon pausas eller när slutet av videon nås, och den beror också på parametern iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet på uppspelningsikonen styrs med följande CSS-klassväljare:

```
.s7video360viewer . s7video360player .s7iconeffect
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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
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

**Exempel**  - Ställ in en 100 x 100 pixlar stor uppspelningsikon.

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
