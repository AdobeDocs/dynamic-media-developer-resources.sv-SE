---
description: JavaScript API-referens för Video Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resurs  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Sträng </span>} nytt resurs-ID, explicit bilduppsättning eller explicit bilduppsättning med bildrutespecifika Image Serving-modifierare, med globala Image Serving-modifierare som tillval efter "?". </p> <p> Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger den nya resursen. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om det anropas efter `init()` byter visningsprogrammet resursen under körning.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referens för en bild:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

En referens till en bilduppsättning som definierats i en katalog:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Explicit bilduppsättning:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explicit bilduppsättning med bildrutespecifika bildservermodifierare:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Skärpemodifierare har lagts till i alla bilder i uppsättningen:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

