---
description: JavaScript API-referens för Video Image Viewer.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva bilder
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# setParam{#setparam}

JavaScript API-referens för Video Image Viewer.

` setParam( *`namn, värde`*)`

Ställer in visningsparametern på ett angivet värde. Parametern är antingen ett visningsprogramspecifikt konfigurationsalternativ eller en programvaruutvecklingsmodifierare. Den här parametern anropas före `init()`.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickades med JSON-objektet `config` till konstruktorn.

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parametrar {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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
<instance>.setParam("style", "etc/dam/presets/css/html5_interactiveimage.css")
```

