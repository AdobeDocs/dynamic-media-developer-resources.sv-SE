---
description: JavaScript API-referens för Basic Zoom Viewer.
seo-description: JavaScript API-referens för Basic Zoom Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: af433f15-34a0-4867-97c5-acab47e3e008
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

JavaScript API-referens för Basic Zoom Viewer.

` setAsset( *`resurs`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tillgång</span></span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nytt resurs-ID, med valfria IS-modifierare efter "?" </p> <p> Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger den nya resursen. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om det anropas efter `init()`byts resursen ut vid körning.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referens för en bild:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Skärpemodifierare har lagts till i alla bilder i uppsättningen:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```

