---
description: JavaScript API-referens för Interactive Video Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
exl-id: 24d8d11d-4688-4ca0-92ae-824a5e984a10
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för Interactive Video Viewer.

`setAsset(asset[, data])`

Anger den nya resursen och valfria ytterligare tillgångsdata. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om det anropas efter `init()` byter visningsprogrammet resursen under körning.

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> resurs  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Sträng </span>} nytt resurs-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data  </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} JSON-objekt med följande valfria fält (skiftlägeskänsliga): </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> posterimage  </span> - Bild som ska visas i den första bildrutan innan videon börjar spelas upp. Se <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> caption  </span> - platsen för den nya bildtextfilen. Om inget anges visas inte bildtextknappen i användargränssnittet. </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> navigation  </span> - URL eller sökväg till WebVTT-navigeringsinnehållet. WebVTT-filen ska hanteras av Image Serving. </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData  </span> - URL eller sökväg till interaktivt WebVTT-datainnehåll. WebVTT-filen måste hanteras av Image Serving. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```
