---
title: setLocalizedTexter
description: JavaScript API-referens för Inline Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: a0d602f5-e698-4dad-af95-70ef5ef88af6
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# setLocalizedTexter{#setlocalizedtexts}

JavaScript API-referens för Inline Zoom Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> JSON-objektet <span class="codeph"> Object </span> med lokaliseringsdata. </p> <p>Mer information finns i <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Lokalisering av användargränssnittselement </a>. </p> <p>Mer information om objektets innehåll finns i <i>användarhandboken för SDK för visningsprogrammet</i> och i exemplet. </p> </td> 
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
