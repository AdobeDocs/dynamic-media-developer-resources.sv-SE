---
description: JavaScript API-referens för eCatalog Viewer.
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Developer,User
exl-id: cbd7987b-5e47-4ac0-8235-a217e5e6dee9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# setParams{#setparams}

JavaScript API-referens för eCatalog Viewer.

[!DNL ` setParams( *`parametrar`*)`]

Anger en eller flera parametrar till ett givet värde. Metodargumentets syntax är identisk med en URL-frågesträng. Det betyder att det representerar namn=värde-par avgränsade med [!DNL `&`]. Precis som i en frågesträng är namnen och värdena procentuellt kodade med UTF8. Innan du anropar [!DNL `init()`] måste den här parametern anropas.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med JSON-objektet [!DNL `config`] till konstruktorn.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
