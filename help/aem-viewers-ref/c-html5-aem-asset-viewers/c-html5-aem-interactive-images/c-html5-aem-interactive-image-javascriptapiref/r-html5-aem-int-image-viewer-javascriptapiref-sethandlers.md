---
description: JavaScript API-referens för Interactive Image Viewer
seo-description: JavaScript API-referens för Interactive Image Viewer
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 93db9c88-890e-4be8-b82f-d15978a0cfac
translation-type: tm+mt
source-git-commit: 323a4f72b5bb46832a569ffad38104bac7da17df
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# setHandlers{#sethandlers}

JavaScript API-referens för Interactive Image Viewer

`setHandlers(handlers)`

Anger noll eller flera callback-hanterare. Ett anrop till den här metoden skriver helt över händelsehanterare som tidigare tilldelats för den visningsprograminstansen. Måste anropas innan `init()`.

## Parameter {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hanterare </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON-objekt med återanrop för visningsprogramhändelse. Egenskapsnamnet är namnet på den visningsprogramhändelse som stöds. Egenskapsvärdet är en JavaScript-funktionsreferens till ett lämpligt återanrop. </p> <p>Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Händelseåteranrop </a> för mer information om visningsprogramhändelser. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

