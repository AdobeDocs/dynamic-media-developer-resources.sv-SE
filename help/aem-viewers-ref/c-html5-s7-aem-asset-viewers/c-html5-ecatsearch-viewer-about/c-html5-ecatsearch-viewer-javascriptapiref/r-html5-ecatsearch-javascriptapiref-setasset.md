---
description: JavaScript API-referens för Video Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för Video Viewer.

[!DNL ` setAsset( *`resurs`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resurs </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> String </span> nytt resurs-ID eller explicit bilduppsättning med tillvalsmodifierare för bildservertillägg efter <span class="codeph"> ? </span>. </p> <p> Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger en ny resurs. Du kan anropa parametern när som helst, antingen före eller efter [!DNL `init()`]. Om den anropas efter [!DNL `init()`] byter visningsprogrammet ut resursen under körning.

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
