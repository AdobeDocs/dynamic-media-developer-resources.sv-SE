---
description: Det grundläggande zoomvisningsprogrammet har stöd för Adobe Analytics-spårning direkt.
seo-description: Det grundläggande zoomvisningsprogrammet har stöd för Adobe Analytics-spårning direkt.
seo-title: Stöd för Adobe Analytics-spårning
solution: Experience Manager
title: Stöd för Adobe Analytics-spårning
topic: Dynamic media
uuid: f48fde77-7e48-4d56-b5c5-079a484e6d9c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Stöd för Adobe Analytics-spårning{#support-for-adobe-analytics-tracking}

Det grundläggande zoomvisningsprogrammet har stöd för Adobe Analytics-spårning direkt.

## Spåra direkt {#section-ba994f079d0343c8ae48adffaa3195a3}

Det enkla zoomvisningsprogrammet har stöd för att [!DNL Adobe Analytics] spåra färdiga filer. Om du vill aktivera spårning skickar du rätt namn på företagets förinställning som `config2` parameter.

Visningsprogrammet skickar även en enda HTTP-begäran för spårning till den konfigurerade Image Server med information om visningsprogramtyp och version.

## Anpassad spårning {#section-cda48fc9730142d0bb3326bac7df3271}

Om du vill integrera med analyssystem från tredje part måste du lyssna på `trackEvent` visningsprogrammets återanrop och bearbeta callback-funktionens `eventInfo` argument efter behov. Följande kod är ett exempel på en sådan hanterarfunktion:

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col2"> <p>en resurs byts ut i visningsprogrammet med <span class="codeph"> setAsset()- </span> API:t. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMA </span> </p> </td> 
   <td colname="col2"> <p> en bild zoomas in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>en bild är panorerad. </p> </td> 
  </tr> 
 </tbody> 
</table>

