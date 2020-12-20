---
description: JavaScript API-referens för Inline Zoom Viewer.
seo-description: JavaScript API-referens för Inline Zoom Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 7bccf2c0-9f9a-47ac-8b53-385989e8267c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# setParam{#setparam}

JavaScript API-referens för Inline Zoom Viewer.

` setParam( *`namn, värde`*)`

Ställer in visningsparametern på ett angivet värde. Parametern är antingen ett visningsprogramspecifikt konfigurationsalternativ eller en programvaruutvecklingsmodifierare. Den här parametern anropas före `init()`. Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med JSON-objektet `config` till konstruktorn.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> parameternamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> parametervärde. Värdet kan inte vara procentkodat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

