---
title: Stöd för Adobe Analytics tracking
description: Utfällbara visningsprogram har stöd för Adobe Analytics-spårning direkt vid leverans.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User,Data Engineer,Data Architect
exl-id: 6b6216f4-34dc-496f-a0c3-e97d48da14c6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# Stöd för Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

Utfällbara visningsprogram har stöd för Adobe Analytics-spårning direkt vid leverans.

## Spåra direkt {#section-ba994f079d0343c8ae48adffaa3195a3}

Den utfällbara visningsprogrammet har stöd för [!DNL Adobe Analytics] spårning direkt. Om du vill aktivera spårning skickar du rätt namn på företagets förinställning som `config2` parameter.

Visningsprogrammet skickar även en enda HTTP-begäran för spårning till den konfigurerade Image Server med information om visningsprogramtyp och version.

## Anpassad spårning {#section-cda48fc9730142d0bb3326bac7df3271}

För att kunna integreras med analyssystem från tredje part måste man lyssna på `trackEvent` återanrop till visningsprogrammet och bearbeta `eventInfo` vid behov callback-funktionens argument. Följande kod är ett exempel på en sådan hanterarfunktion:

```javascript {.line-numbers}
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
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
   <td colname="col2"> <p>visningsprogrammet först läses in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>en resurs byts ut i visningsprogrammet med <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMA </span> </p> </td> 
   <td colname="col2"> <p>den utfällbara menyn aktiveras eller zoomnivån ändras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p> en bild är panorerad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FÄRGRUTA </span> </p> </td> 
   <td colname="col2"> <p> en bild ändras genom att man klickar eller trycker på en färgruta. </p> </td> 
  </tr> 
 </tbody> 
</table>
