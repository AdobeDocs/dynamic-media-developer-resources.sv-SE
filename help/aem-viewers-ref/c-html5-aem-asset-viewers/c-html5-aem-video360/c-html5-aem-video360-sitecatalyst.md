---
title: Stöd för Adobe Analytics tracking
description: Stöd för Adobe Analytics tracking
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Stöd för Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

Som standard skickar visningsprogrammet en enda HTTP-begäran för spårning till den konfigurerade Image-servern med information om visningsprogramtyp och version.

## Anpassad spårning {#section-cda48fc9730142d0bb3326bac7df3271}

Om du vill integrera med analyssystem från tredje part måste du lyssna på `trackEvent`-visningsåteranropet och bearbeta `eventInfo`-argumentet för återanropsfunktionen efter behov. Följande kod är ett exempel på en sådan hanterarfunktion:

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   case "INTERACTIVE_SWATCH": 
    //custom event processing code which handles user clicks on interactive swatches 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

Visningsprogrammet spårar följande SDK-användarhändelser:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK-användarhändelse </p> </th> 
   <th colname="col2" class="entry"> <p>Skickat... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LÄS IN </span> </p> </td> 
   <td colname="col2"> <p>när visningsprogrammet läses in först. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>när en resurs byts ut i visningsprogrammet med API:t <span class="codeph"> setAsset() </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPELA UPP </span> </p> </td> 
   <td colname="col2"> <p>när uppspelningen startar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>när uppspelningen pausas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>när uppspelningen stoppas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>när uppspelningen når en av följande milstolpar: 0 %, 25 %, 50 %, 75 % eller 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERACTIVE_SWATCH </span> </p> </td> 
   <td colname="col2"> <p>varje gång användaren klickar på en interaktiv färgruta. </p> </td> 
  </tr> 
 </tbody> 
</table>
