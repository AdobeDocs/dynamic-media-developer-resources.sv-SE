---
description: JavaScript API-referens för Video Viewer.
solution: Experience Manager
title: VideoViewer
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Video
role: Developer,User
exl-id: 4ba152e6-b5a9-4e81-b9f8-aa987a1c31f9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 1%

---

# VideoViewer{#videoviewer}

JavaScript API-referens för Video Viewer.

`VideoViewer([config])`

Konstruktor; skapar en ny Video Viewer-instans.

## Parametrar {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}-konfigurationsobjekt ( </span> valfritt) gör att alla visningsprograminställningar kan skickas till konstruktorn och att enskilda set-metoder inte kan anropas. Innehåller följande egenskaper: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID för DOM-behållaren (vanligtvis en  <span class="codeph"> DIV  </span>) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när <span class="codeph"> init() </span> körs. Obligatoriskt. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON-objekt med visarkonfigurationsparametrar där egenskapsnamnet antingen är ett visningsprogramspecifikt konfigurationsalternativ eller en SDK-modifierare, och värdet för den egenskapen är ett motsvarande inställningsvärde. Obligatoriskt. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> hanterare  </span> -  <span class="codeph"> {Object}  </span> JSON-objekt med återkopplingar för visningsprogramhändelser, där egenskapsnamnet är namnet på den visningsprogramhändelse som stöds och egenskapsvärdet är en JavaScript-funktionsreferens till ett lämpligt återanrop. Valfritt. <p>Mer information om visningsprogramhändelser finns i <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Händelseåteranrop </a>. </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Object  </span>} JSON-objekt med lokaliseringsdata. Valfritt. </p> <p>Mer information finns i <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> SDK-namnområdet för visningsprogrammet </a>. </p> <p>Mer information om objektets innehåll finns i <i>användarhandboken för SDK för visningsprogrammet</i> och exemplet. Valfritt. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
