---
description: JavaScript API-referens för Spin Viewer.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Visningsprogram,SDK/API,snurra uppsättningar
role: Developer,User
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# setParam{#setparam}

JavaScript API-referens för Spin Viewer.

` setParam( *`namn, värde`*)`

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

Ställer in visningsparametern på ett angivet värde. Parametern är antingen ett visningsprogramspecifikt konfigurationsalternativ eller en programvaruutvecklingsmodifierare. Den här parametern anropas före `init()`.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med JSON-objektet `config` till konstruktorn.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
