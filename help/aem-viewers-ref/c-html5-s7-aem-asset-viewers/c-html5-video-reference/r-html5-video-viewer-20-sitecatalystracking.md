---
description: Video Viewer stöder Adobe Analytics-spårning direkt.
seo-description: Video Viewer stöder Adobe Analytics-spårning direkt.
seo-title: Stöd för Adobe Analytics-spårning
solution: Experience Manager
title: Stöd för Adobe Analytics-spårning
topic: Dynamic media
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Stöd för Adobe Analytics-spårning{#support-for-adobe-analytics-tracking}

Video Viewer stöder Adobe Analytics-spårning direkt.

## Spåra direkt {#section-3b101fe30be943c1b679fd5c273569ca}

Video Viewer stöder Adobe Analytics-spårning direkt.

Om du vill aktivera spårning skickar du rätt namn på företagets förinställning som `config2` parameter.

Visningsprogrammet skickar även en enda HTTP-begäran för spårning till den konfigurerade Image Server med information om visningsprogramtyp och version.

## Anpassad spårning {#section-ab10bd7caf184721a366cf3953071934}

Om du vill integrera med analyssystem från tredje part måste du lyssna efter `trackEvent` återanrop och processargument `eventInfo` för återanropsfunktionen efter behov. Följande kod är ett exempel på en sådan hanterarfunktion:

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
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
   <th colname="col2" class="entry"> <p>Skickat när.. </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LADDA </span> </p> </td> 
   <td colname="col2"> <p>visningsprogrammet läses in först. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>en resurs byts ut i visningsprogrammet med <span class="codeph"> setAsset()- </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPELA </span> </p> </td> 
   <td colname="col2"> <p>uppspelningen startas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUS </span> </p> </td> 
   <td colname="col2"> <p>uppspelningen är pausad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>uppspelningen stoppas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTON </span> </p> </td> 
   <td colname="col2"> <p>uppspelningen når en av följande millisekunder: 0 %, 25 %, 50 %, 75 % och 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

