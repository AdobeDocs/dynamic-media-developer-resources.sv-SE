---
title: SpinViewer
description: JavaScript API-referens för Spin Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 0cfde665-c578-41a0-a428-0db3cbdac6ae
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# SpinViewer{#spinviewer}

JavaScript API-referens för Spin Viewer.

`SpinViewer([config])`

Konstruktor, skapar en ny Spin Viewer-instans.

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> valfritt JSON-konfigurationsobjekt, tillåter att alla visningsprograminställningar skickas till konstruktorn och undviker att anropa enskilda set-metoder. Innehåller följande egenskaper: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID för DOM-behållaren (vanligtvis en <span class="codeph"> DIV </span>) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när <span class="codeph"> init() </span> körs. Obligatoriskt. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON-objekt med visarkonfigurationsparametrar där egenskapsnamnet antingen är ett visningsprogramspecifikt konfigurationsalternativ eller en SDK-modifierare, och värdet för den egenskapen är ett motsvarande inställningsvärde. Obligatoriskt. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph">-hanterare </span> - <span class="codeph"> {Object} </span> JSON-objekt med återanrop för visningsprogramhändelser, där egenskapsnamnet är namnet på den visningsprogramhändelse som stöds och egenskapsvärdet är en JavaScript-funktionsreferens till ett lämpligt återanrop. Valfritt. </p> <p>Mer information om visningsprogramhändelser finns i <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> Händelseåteranrop </a>. </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> JSON-objekt med lokaliseringsdata. Valfritt. </p> <p>Mer information finns i <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Lokalisering av användargränssnittselement </a>. </p> <p>Mer information om objektets innehåll finns även i <i>användarhandboken för visningsprogrammet för SDK</i> och i exemplet. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
