---
description: JavaScript API-referens för visningsprogrammet för smart beskärning.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för visningsprogrammet för smart beskärning.

`setAsset(asset[, data])`

Anger den nya resursen och valfria ytterligare tillgångsdata. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om den anropas efter `init()`byter visningsprogrammet ut resursen vid körning.

Se även [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref\r-html5-aem-smartcropvideo-viewer-javascriptapiref-init. md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parametrar {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> resurs </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Sträng </span>} nytt resurs-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON-objekt med följande valfria fält (skiftlägeskänsliga): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span> - Bild som ska visas i den första bildrutan innan videon börjar spelas upp. Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-cmdref/r-html5-aem-smartcropvideo-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> bildtext </span> - platsen för den nya undertextningsfilen. Om filen inte anges visas inte den stängda bildtextsknappen i användargränssnittet. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
