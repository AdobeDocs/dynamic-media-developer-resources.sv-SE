---
title: PanoramavyViewer
description: Konstruktor, skapar en HTML5 Panoramic Viewer-instans.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# PanoramavyViewer{#panoramicviewer}

`PanoramicViewer([config])`
Konstruktor, skapar en HTML5 Panoramic Viewer-instans.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} valfria JSON-konfigurationsobjekt, gör att du kan skicka alla visningsprograminställningar till konstruktorn och undvika att anropa enskilda set-metoder. Den innehåller följande egenskaper:

* containerId - {String} ID för DOM-behållaren (vanligtvis en DIV) som visningsprogrammet infogas i. Du behöver inte ha behållarelementet som skapas när metoden anropas, men behållaren måste finnas när init() körs. Obligatoriskt
* params - {Object} JSON-objekt med visarkonfigurationsparametrar där egenskapsnamnet antingen är visningsprogramsspecifikt konfigurationsalternativ eller SDK modifier, och värdet för den egenskapen är ett motsvarande inställningsvärde. Obligatoriskt
* hanterare - {Object} JSON-objekt med återanrop för visningsprogramhändelse, där egenskapsnamnet är namnet på den visningsprogramhändelse som stöds och egenskapsvärdet är en JavaScript-funktionsreferens till rätt återanrop. Mer information om visningsprogramhändelser finns i avsnittet Händelseåteranrop. Valfritt.


## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
