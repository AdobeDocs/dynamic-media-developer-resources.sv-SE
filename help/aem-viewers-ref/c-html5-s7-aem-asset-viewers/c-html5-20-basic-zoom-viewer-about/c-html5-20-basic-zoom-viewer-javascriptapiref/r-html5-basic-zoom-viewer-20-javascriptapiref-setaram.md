---
description: JavaScript API-referens för Basic Zoom Viewer.
seo-description: JavaScript API-referens för Basic Zoom Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
uuid: 9e3fa66f-2817-4969-9532-99cd75b3e22a
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# setParam{#setparam}

JavaScript API-referens för Basic Zoom Viewer.

` setParam( *`namn, värde`*)`

Ställer in visningsparametern på ett angivet värde. Parametern är antingen ett visningsprogramspecifikt konfigurationsalternativ eller en programvaruutvecklingsmodifierare. Den här parametern anropas före `init()`.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickades med JSON-objektet `config` till konstruktorn.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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

