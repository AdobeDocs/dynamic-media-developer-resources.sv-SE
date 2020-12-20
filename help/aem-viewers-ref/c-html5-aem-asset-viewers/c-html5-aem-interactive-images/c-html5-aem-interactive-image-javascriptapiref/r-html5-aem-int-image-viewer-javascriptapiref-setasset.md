---
description: JavaScript API-referens för Video Image Viewer.
seo-description: JavaScript API-referens för Video Image Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8cb10b2e-addb-4659-a93b-5a53d0f8a5bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# setAsset{#setasset}

JavaScript API-referens för Video Image Viewer.

` setAsset( *`resurs`*)`

Anger den nya resursen. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om det anropas efter `init()` byter visningsprogrammet resursen under körning.

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resurs</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Sträng</span>} nytt resurs-ID. </p> <p>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av detta visningsprogram. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referens för en bild:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```

