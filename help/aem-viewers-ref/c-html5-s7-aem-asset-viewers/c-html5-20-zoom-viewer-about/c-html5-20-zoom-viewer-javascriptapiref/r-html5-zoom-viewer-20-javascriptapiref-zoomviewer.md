---
title: ZoomViewer
description: JavaScript API-referens för Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: fa52a017-0748-4e4f-8d91-ad1529fbfbdb
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# ZoomViewer{#zoomviewer}

JavaScript API-referens för Zoom Viewer.

`ZoomViewer([config])`

Konstruktor, skapar en Zoom Viewer-instans.

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> valfritt JSON-konfigurationsobjekt, gör att alla visningsprograminställningar kan skickas till konstruktorn för att undvika anrop av enskilda set-metoder. Innehåller följande egenskaper: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID för DOM-behållaren (vanligtvis en <span class="codeph"> DIV </span>) som visningsprogrammet infogas i. När den här metoden anropas är det inte nödvändigt att skapa behållarelementet. Behållaren måste dock finnas när <span class="codeph"> init() </span> körs. Obligatoriskt. </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <span class="codeph"> parametrar </span> - <span class="codeph"> {Object} </span> JSON-objekt med visarkonfigurationsparametrar där egenskapsnamnet antingen är visningsprogramspecifikt konfigurationsalternativ eller SDK-modifierare, och värdet för den egenskapen är ett motsvarande inställningsvärde. Obligatoriskt. </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <span class="codeph"> hanterare </span> - <span class="codeph"> {Object} </span> JSON-objekt med återanrop för visningsprogramhändelser, där egenskapsnamnet är namnet på den visningsprogramhändelse som stöds och egenskapsvärdet är en JavaScript-funktionsreferens till lämpligt återanrop. Valfritt. <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Händelseåteranrop </a> för mer information om visningsprogramhändelser. </p> </li> 
      <li id="li_1D181A6B1D434B29B09AFD3F4BE059BD"> <span class="codeph"> localizedTexter </span> - <span class="codeph"> {Object} </span> JSON-objekt med lokaliseringsdata. Valfritt. <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisering av användargränssnittselement </a> för mer information. </p> <p>Se även <i>Användarhandbok för Viewer SDK</i> och exemplet innehåller mer information om objektets innehåll. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```
