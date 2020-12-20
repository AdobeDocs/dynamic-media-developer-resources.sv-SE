---
description: JavaScript API-referens för Inline Zoom Viewer.
seo-description: JavaScript API-referens för Inline Zoom Viewer.
seo-title: setLocalizedTexter
solution: Experience Manager
title: setLocalizedTexter
topic: Dynamic media
uuid: 3e02e20f-2e81-4b4d-bf2a-cee8998faafb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# setLocalizedTexter{#setlocalizedtexts}

JavaScript API-referens för Inline Zoom Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Objektet </span>} JSON-objekt med lokaliseringsdata. </p> <p>Mer information finns i <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Lokalisering av användargränssnittselement </a>. </p> <p>Mer information om objektets innehåll finns i <i>användarhandboken för SDK för visningsprogrammet</i> och exemplet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger SYMBOL-värden för lokalisering för en eller flera språkinställningar. Den här parametern måste anropas före `init()`.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```

