---
title: setHandlers
description: JavaScript API-referens för visningsprogrammet för blandade media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e30f1b73-1dba-4d4c-9e90-f343ca404550
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# setHandlers{#sethandlers}

JavaScript API-referens för visningsprogrammet för blandade media.

`setHandlers(handlers)`

Anger noll eller flera callback-hanterare. Ett anrop till den här metoden skriver helt över händelsehanterare som tidigare tilldelats för den visningsprograminstansen. Måste anropas före `init()`.

## Parameter {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hanterare </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON-objekt med återkopplingar för visningsprogramhändelser, där egenskapsnamnet är namnet på den visningsprogramhändelse som stöds och egenskapsvärdet är en JavaScript-funktionsreferens till ett lämpligt återanrop. </p> <p>Mer information om visningsprogramhändelser finns i <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> Händelseåteranrop </a>. </p> </td> 
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
