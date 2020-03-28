---
description: JavaScript API-referens för blandad Media Viewer.
seo-description: JavaScript API-referens för blandad Media Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8c341a8a-25b5-4db9-ad1a-919ded79f2ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

JavaScript API-referens för blandad Media Viewer.

` setAsset( *`resurs`*[,data]))`

Anger den nya resursen och valfria ytterligare tillgångsdata. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om det anropas efter `init()`byts resursen ut vid körning.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parametrar {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`resurs`*` - { `String`} nytt resurs-ID eller explicit blandad mediamängd, med tillvalsmodifierare för Image Serving tillagda efter `?`.

Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet.

` *`data`*` - { `JSON`} plats för den nya bildtextfilen.

Om inget anges visas inte bildtextknappen i användargränssnittet. De bildtexter som anges med den här parametern gäller för den video som kommer först i den blandade medieuppsättningen. efterföljande videofilmer spelas upp utan bildtexter. Detta visningsprogram stöder följande komponent-ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponent-ID </p> </th> 
   <th colname="col2" class="entry"> <p>Namn på SDK-komponentklass för visningsprogram </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage </span> </p> </td> 
   <td colname="col2"> <p>Bild som ska visas i den första bildrutan innan videon börjar spelas upp. </p> <p>Se <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bildtext </span> </p> </td> 
   <td colname="col2"> <p> Platsen för den nya bildtextfilen. </p> <p>Om inget anges visas inte bildtextknappen i användargränssnittet. Bildtexter som anges med den här parametern gäller för videon som kommer först i medieuppsättningen. Efterföljande videofilmer spelas upp utan bildtexter. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referens för en medieuppsättning:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Explicit medieuppsättning:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Skärpemodifierare har lagts till i alla bilder i uppsättningen:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

