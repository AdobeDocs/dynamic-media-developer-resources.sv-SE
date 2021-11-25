---
title: setAsset
description: JavaScript API-referens för panoramavisningsprogrammet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för panoramavisningsprogrammet.

`setAsset(asset)`

Anger den nya resursen. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om den anropas efter `init()`byter visningsprogrammet ut resursen vid körning.

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-javascriptapiref/r-html5-aem-panoramic-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> resurs </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Sträng</span>} nytt resurs-ID. Bilder som använder bildåtergivning (IR) eller användargenererat innehåll (UGC) stöds inte av det här visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/PanoramicImage-Sample")
```
