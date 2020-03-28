---
description: JavaScript API-referens för Basic Zoom Viewer.
seo-description: JavaScript API-referens för Basic Zoom Viewer.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 8c2a740f-deed-4f03-9405-36533ba1b0aa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

JavaScript API-referens för Basic Zoom Viewer.

` setParams( *`parametrar`*)`

Anger en eller flera parametrar till ett givet värde. Metodargumentets syntax är identisk med en URL-frågesträng. Det betyder att den representerar namn=värde-par avgränsade med `&`. Precis som i en frågesträng är namnen och värdena procentuellt kodade med UTF8. Innan du anropar `init()`måste den här parametern anropas.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickades med `config` JSON-objektet till konstruktorn.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parametrar</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value-parameterpar avgränsade med <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```

