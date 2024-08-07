---
title: setAsset
description: JavaScript API-referens för Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för Video Viewer.

` setAsset( *`resurs`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resurs </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> String </span> nytt resurs-ID eller explicit bilduppsättning med tillvalsmodifierare för bildservertillägg efter <span class="codeph"> ? </span>. </p> <p> Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger en ny resurs. Du kan anropa parametern när som helst, antingen före eller efter `init()`. Om den anropas efter `init()` byter visningsprogrammet ut resursen under körning.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

En referens till en bilduppsättning som definierats i en katalog:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Explicit bilduppsättning, med förkombinerade sidor:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Explicit bilduppsättning, med enskilda sidbilder:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Skärpemodifierare har lagts till i alla bilder i uppsättningen:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
