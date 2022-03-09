---
title: Stöd för analysspårning
description: Stöd för analysspårning
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User,Data Engineer,Data Architect
exl-id: 17e8937f-e328-46a4-b7d9-1fd39ab2e8bd
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# Stöd för analysspårning{#support-for-analytics-tracking}

## Anpassad spårning {#section-cda48fc9730142d0bb3326bac7df3271}

Som standard skickar visningsprogrammet en enda HTTP-begäran för spårning till konfigurerad Image Server med information om visningsprogramtyp och version.

För att kunna integreras med analyssystem från tredje part måste man lyssna på `trackEvent` återanrop till visningsprogrammet och bearbeta `eventInfo` vid behov callback-funktionens argument. Följande kod är ett exempel på en sådan hanterarfunktion:

```javascript {.line-numbers}
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>användaren aktiverar hotspot. </p> </td> 
  </tr> 
 </tbody> 
</table>
