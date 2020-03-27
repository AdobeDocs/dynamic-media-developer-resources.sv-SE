---
description: JavaScript API-referens för Basic Zoom Viewer.
seo-description: JavaScript API-referens för Basic Zoom Viewer.
seo-title: setLocalizedTexter
solution: Experience Manager
title: setLocalizedTexter
topic: Dynamic media
uuid: 34a2ea4e-5493-41fa-92bf-5cebe66f6370
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedTexter{#setlocalizedtexts}

JavaScript API-referens för Basic Zoom Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span></span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON-objekt med lokaliseringsdata. </p> <p>Mer information finns <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> i Lokalisering av användargränssnittselement</a> . </p> <p> Se även användarhandboken <i>för</i> visningsprogrammet SDK och exemplet för mer information om objektets innehåll. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger SYMBOL-värden för lokalisering för en eller flera språkinställningar. Den här parametern måste anropas före `init()`.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

