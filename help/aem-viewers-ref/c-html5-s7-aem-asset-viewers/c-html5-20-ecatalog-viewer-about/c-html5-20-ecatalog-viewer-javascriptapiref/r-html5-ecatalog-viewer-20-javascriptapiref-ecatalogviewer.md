---
description: JavaScript API-referens för eCatalog Viewer.
seo-description: JavaScript API-referens för eCatalog Viewer.
seo-title: eCatalogViewer
solution: Experience Manager
title: eCatalogViewer
topic: Dynamic media
uuid: b87b6f6b-3e83-47b3-b867-30eca5eae56b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# eCatalogViewer{#ecatalogviewer}

JavaScript API-referens för eCatalog Viewer.

`eCatalogViewer([config])`

Konstruktorn skapar en ny eCatalog Viewer-instans.

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> valfritt JSON-konfigurationsobjekt, tillåter att alla visningsprograminställningar skickar till konstruktorn och undviker att anropa enskilda set-metoder. Innehåller följande egenskaper: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID för DOM-behållaren (vanligtvis en <span class="codeph"> DIV </span>) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när <span class="codeph"> init() </span> körs. Obligatoriskt. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON-objekt med visarkonfigurationsparametrar där egenskapsnamnet antingen är ett visningsprogramsspecifikt konfigurationsalternativ eller en SDK-modifierare, och värdet för den egenskapen är ett motsvarande inställningsvärde. Obligatoriskt. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> hanterare </span> - <span class="codeph"> {Object} </span> JSON-objekt med återanrop till visningsprogramhändelser, där egenskapsnamnet är namnet på den visningsprogramhändelse som stöds och egenskapsvärdet är en JavaScript-funktionsreferens till ett lämpligt återanrop. Valfritt. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> Händelseåteranrop </a> för mer information om visningsprogramhändelser. </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Object </span>} JSON-objekt med lokaliseringsdata. Valfritt. </p> <p>Mer information finns i Lokalisering av element i användargränssnittet <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> </a> . </p> <p>Se även användarhandboken <i>för</i> visningsprogrammet SDK och exemplet för mer information om objektets innehåll. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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

