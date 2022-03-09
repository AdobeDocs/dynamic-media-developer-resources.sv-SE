---
title: Stöd för Adobe Analytics tracking
description: Video Viewer har stöd för körklar Adobe Analytics-spårning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# Stöd för Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

Video Viewer har stöd för körklar Adobe Analytics-spårning.

## Spåra direkt {#section-3b101fe30be943c1b679fd5c273569ca}

Video Viewer har stöd för körklar Adobe Analytics-spårning.

Om du vill aktivera spårning skickar du rätt namn på företagets förinställning som `config2` parameter.

Visningsprogrammet skickar även en enda HTTP-begäran för spårning till den konfigurerade Image Server med information om visningsprogramtyp och version.

## Anpassad spårning {#section-ab10bd7caf184721a366cf3953071934}

För att kunna integreras med analyssystem från tredje part måste man lyssna på `trackEvent` återanrop och process för visningsprogram `eventInfo` vid behov callback-funktionens argument. Följande kod är ett exempel på en sådan hanterarfunktion:

```javascript {.line-numbers}
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
   <td colname="col2"> <p>en resurs byts ut i visningsprogrammet med <span class="codeph"> setAsset() </span> API. </p> </td> 
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
