---
title: setAsset
description: JavaScript API-referens för visningsprogrammet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för visningsprogrammet.

` setAsset( *`resurs`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resurs </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> String </span> nytt resurs-ID, explicit bilduppsättning eller explicit bilduppsättning med bildrutespecifika Image Serving-modifierare, med globala Image Serving-modifierare som tillval efter <span class="codeph"> ?</span>. </p> <p> Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger den nya resursen. Du kan anropa parametern när som helst, antingen före eller efter `init()`. Om den anropas efter `init()` byter visningsprogrammet ut resursen under körning.

Se även [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

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

Explicit bilduppsättning enligt följande:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explicit bilduppsättning med bildrutespecifika bildservermodifierare:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Skärpemodifierare har lagts till i alla bilder i uppsättningen:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
