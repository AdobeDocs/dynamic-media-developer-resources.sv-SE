---
title: setHandlers
description: JavaScript API-referens för Interactive Image Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: a5e42842-dc88-454b-8229-33a65c01bf88
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# setHandlers{#sethandlers}

JavaScript API-referens för Interactive Image Viewer

`setHandlers(handlers)`

Anger noll eller flera callback-hanterare. Ett anrop till den här metoden skriver helt över händelsehanterare som tidigare tilldelats för den visningsprograminstansen. Måste anropas före `init()`.

## Parameter {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hanterare  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}  </span> JSON-objekt med återanrop för visningsprogramhändelser. Egenskapsnamnet är namnet på den visningsprogramhändelse som stöds. Egenskapsvärdet är en JavaScript-funktionsreferens till ett lämpligt återanrop. </p> <p>Mer information om visningsprogramhändelser finns i <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Händelseåteranrop </a>. </p> </td> 
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
