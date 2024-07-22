---
title: setAsset
description: JavaScript API-referens för Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för Video Viewer.

` setAsset( *`resurs`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resurs </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> String </span> nytt resurs-ID, explicit bilduppsättning eller explicit bilduppsättning med bildrutespecifika Image Serving-modifierare, med globala Image Serving-modifierare som tillval efter "?". </p> <p> Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger den nya resursen. Du kan anropa parametern när som helst, antingen före eller efter `init()`. Om den anropas efter `init()` byter visningsprogrammet ut resursen under körning.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

En bildreferens enligt följande:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

En referens till en bilduppsättning som definierats i en katalog enligt följande:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Explicit bilduppsättning enligt följande:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explicit bilduppsättning med bildrutespecifika bildservermodifierare enligt följande:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Skärpemodifieraren har lagts till i alla bilder i uppsättningen enligt följande:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
