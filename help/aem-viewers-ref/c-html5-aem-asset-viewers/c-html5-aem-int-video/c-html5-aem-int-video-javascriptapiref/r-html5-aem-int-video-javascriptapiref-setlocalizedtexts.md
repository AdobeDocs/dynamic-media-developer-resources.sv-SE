---
description: JavaScript API-referens för Interactive Video Viewer.
seo-description: JavaScript API-referens för Interactive Video Viewer.
seo-title: setLocalizedTexter
solution: Experience Manager
title: setLocalizedTexter
uuid: 11844a71-adb0-42a9-9b58-b69821070fd2
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# setLocalizedTexter{#setlocalizedtexts}

JavaScript API-referens för Interactive Video Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

Anger SYMBOL-värden för lokalisering för en eller flera språkinställningar. Den här parametern måste anropas före `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Objektet </span>} JSON-objekt med lokaliseringsdata. </p> <p>Mer information finns i <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisering av användargränssnittselement </a>. </p> <p>Se även <i>Användarhandboken för visningsprogrammet SDK</i> och exemplet för mer information om objektets innehåll. </p> </td> 
  </tr> 
 </tbody> 
</table>

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

