---
title: InteractiveVideoViewer
description: JavaScript API-referens för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: efd0ffea-482c-4af4-ac77-ac1b7f326ce9
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# InteractiveVideoViewer{#interactivevideoviewer}

JavaScript API-referens för Interactive Video Viewer.

`InteractiveVideoViewer([config])`

Konstruktor, skapar en Interactive Video Viewer-instans.

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> valfritt JSON-konfigurationsobjekt gör att alla visningsprograminställningar kan skickas till konstruktorn för att undvika att anropa enskilda set-metoder. Innehåller följande egenskaper: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID för DOM-behållaren (vanligtvis en <span class="codeph"> DIV </span>) som visningsprogrammet infogas i. När den här metoden anropas behöver behållarelementet inte skapas. Behållaren måste dock finnas när <span class="codeph"> init() </span> körs. </p> <p>Obligatoriskt. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON-objekt med visarkonfigurationsparametrar där egenskapsnamnet antingen är visningsprogramspecifikt konfigurationsalternativ eller SDK-modifierare, och värdet för den egenskapen är ett motsvarande inställningsvärde. </p> <p>Obligatoriskt. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph">-hanterare </span> - <span class="codeph"> {Object} </span> JSON-objekt med återanrop för visningsprogramhändelser, där egenskapsnamnet är namnet på den visningsprogramhändelse som stöds och egenskapsvärdet är en JavaScript-funktionsreferens till rätt återanrop. </p> <p>Valfritt. </p> <p>Mer information om visningsprogramhändelser finns i <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Händelseåteranrop </a>. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> JSON-objekt med lokaliseringsdata. Valfritt. </p> <p>Mer information finns i <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisering av användargränssnittselement </a>. </p> <p>Mer information om objektets innehåll finns även i <i>användarhandboken för visningsprogrammet för SDK</i> och i exemplet. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
