---
description: JavaScript API-referens för Carousel Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Utvecklare,Affärsledare
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för Carousel Viewer.

` setAsset( *`resurs`*)`

Anger den nya resursen. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om det anropas efter `init()` byter visningsprogrammet resursen under körning.

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resurs</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Sträng</span>} nytt resurs-ID. </p> <p>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referens för en bild:

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```
