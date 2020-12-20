---
description: JavaScript API-referens för Interactive Video Viewer.
seo-description: JavaScript API-referens för Interactive Video Viewer.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 0a5b9798-0e3f-4310-9b6e-0214a420951b
translation-type: tm+mt
source-git-commit: 94b8dde58cda2670f3e2f22f217599c23601e450
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# setParams{#setparams}

JavaScript API-referens för Interactive Video Viewer.

` setParams( *`parametrar`*)`

Anger en eller flera parametrar till ett givet värde. Metodargumentets syntax är identisk med en URL-frågesträng. Det betyder att det representerar namn=värde-par avgränsade med `&`. Precis som i en frågesträng är namnen och värdena procentuellt kodade med UTF8. Innan du anropar `init()` måste den här parametern anropas.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickades med JSON-objektet `config` till konstruktorn.

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).


## Parametern {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parametrar</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value-parameterpar avgränsade med  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
