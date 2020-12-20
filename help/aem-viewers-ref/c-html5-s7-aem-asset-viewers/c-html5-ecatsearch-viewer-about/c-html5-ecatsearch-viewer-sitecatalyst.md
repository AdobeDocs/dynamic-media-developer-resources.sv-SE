---
description: Visningsprogrammet för eCatalog-sökning stöder Adobe Analytics-spårning direkt.
seo-description: Visningsprogrammet för eCatalog-sökning stöder Adobe Analytics-spårning direkt.
seo-title: Stöd för Adobe Analytics tracking
solution: Experience Manager
title: Stöd för Adobe Analytics tracking
topic: Dynamic media
uuid: 2e1e2bc6-5372-4ba2-b6d7-8b760b1b0a8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Stöd för Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

Visningsprogrammet för eCatalog-sökning stöder Adobe Analytics-spårning direkt.

## Spåra {#section-ba994f079d0343c8ae48adffaa3195a3} direkt

Visningsprogrammet för eCatalog-sökning har stöd för [!DNL Adobe Analytics]-spårning som är körklar. Om du vill aktivera spårning skickar du rätt namn på företagets förinställning som `config2`-parameter.

Visningsprogrammet skickar även en enda HTTP-begäran för spårning till den konfigurerade Image Server med information om visningsprogramtyp och version.

## Anpassad spårning {#section-cda48fc9730142d0bb3326bac7df3271}

Om du vill integrera med analyssystem från tredje part måste du lyssna på `trackEvent`-återanropet för visningsprogrammet och bearbeta `eventInfo`-argumentet för återanropsfunktionen efter behov. Följande kod är ett exempel på en sådan hanterarfunktion:

```
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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
   <td colname="col1"> <p> <span class="codeph"> LADDA  </span> </p> </td> 
   <td colname="col2"> <p>visningsprogrammet läses in först. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP  </span> </p> </td> 
   <td colname="col2"> <p>en resurs byts ut i visningsprogrammet med hjälp av API:t <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMA  </span> </p> </td> 
   <td colname="col2"> <p> en bild zoomas in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN  </span> </p> </td> 
   <td colname="col2"> <p>en bild är panorerad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FÄRGRUTA  </span> </p> </td> 
   <td colname="col2"> <p> en bild ändras genom att man klickar eller trycker på en färgruta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SIDA  </span> </p> </td> 
   <td colname="col2"> <p> en aktuell ram ändras i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> OBJEKT  </span> </p> </td> 
   <td colname="col2"> <p>ett popup-fönster med infopanelen är aktiverat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF  </span> </p> </td> 
   <td colname="col2"> <p>en användare navigerar till en annan sida genom att klicka på bildschemat. </p> </td> 
  </tr> 
 </tbody> 
</table>

