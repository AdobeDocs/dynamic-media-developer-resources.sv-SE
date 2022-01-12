---
title: setParams
description: JavaScript API-referens för Inline Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: eb3298da-f19d-4013-8192-c51144d8b866
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# setParams{#setparams}

JavaScript API-referens för Inline Zoom Viewer.

` setParams( *`parametrar`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parametrar</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value, parameterpar avgränsade med <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger en eller flera parametrar till ett givet värde. Metodargumentets syntax är identisk med en URL-frågesträng. Det betyder att den representerar namn=värde-par avgränsade med `&`. Samma som i en frågesträng, namn och värden kodas i procent med UTF8. Innan du ringer `init()`måste den här parametern anropas. Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med `config` JSON-objekt till konstruktorn.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```
