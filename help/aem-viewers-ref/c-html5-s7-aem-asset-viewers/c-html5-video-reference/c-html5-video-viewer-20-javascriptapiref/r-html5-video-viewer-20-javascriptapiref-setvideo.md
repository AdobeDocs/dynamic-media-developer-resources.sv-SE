---
title: setVideo
description: JavaScript API-referens för Video Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c89099f6-09f7-4d81-939e-90ffa2764c8c
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# setVideo{#setvideo}

JavaScript API-referens för Video Viewer

`setVideo(videoUrl[, data])`

Anger ny extern video och ytterligare videodata som tillval. Kan anropas när som helst, både före och efter `init()`. Om anropas efter `init()`byter visningsprogrammet ut videon under körning.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parametrar {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Sträng </span>} en absolut URL till den nya videon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON-objekt med följande valfria fält (skiftlägeskänsliga): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span> - Bild som ska visas i den första bildrutan innan videon börjar spelas upp. Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> bildtext </span> - Plats för den nya bildtextfilen. Om ingen bildtextfil har angetts visas inte bildtextknappen i användargränssnittet. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> navigering </span> - URL eller sökväg till WebVTT-navigeringsinnehåll. WebVTT-filen ska hanteras av Image Serving. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```
