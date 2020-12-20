---
description: JavaScript API-referens för Video360 Viewer.
seo-description: JavaScript API-referens för Video360 Viewer.
seo-title: setLocalizedTexter
solution: Experience Manager
title: setLocalizedTexter
topic: Dynamic media
uuid: dd9cf899-8855-463b-a142-698fd1a650fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# setLocalizedTexter{#setlocalizedtexts}

JavaScript API-referens för Video360 Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

Anger SYMBOL-värden för lokalisering för en eller flera språkinställningar. Den här parametern måste anropas före `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Objektet </span>} JSON-objekt med lokaliseringsdata. </p> <p>Mer information finns i <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Lokalisering av användargränssnittselement </a>. </p> <p>Se även <i>Användarhandboken för visningsprogrammet SDK</i> och exemplet för mer information om objektets innehåll. </p> </td> 
  </tr> 
 </tbody> 
</table>

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

