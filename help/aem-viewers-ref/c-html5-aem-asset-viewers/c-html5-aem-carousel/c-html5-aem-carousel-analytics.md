---
description: Stöd för Adobe Analytics tracking
solution: Experience Manager
title: Stöd för Adobe Analytics tracking
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Utvecklare,Affärsledare,datatekniker,dataarkitekt
exl-id: 9e321684-4861-4d81-b55c-66c77635930e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Stöd för Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

## Anpassad spårning {#section-cda48fc9730142d0bb3326bac7df3271}

Som standard skickar visningsprogrammet en enda HTTP-begäran för spårning till konfigurerad Image Server med information om visningsprogramtyp och version.

Om du vill integrera med analyssystem från tredje part måste du lyssna på `trackEvent`-återanropet för visningsprogrammet och bearbeta `eventInfo`-argumentet för återanropsfunktionen efter behov. Följande kod är ett exempel på en sådan hanterarfunktion:

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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
   <td colname="col2"> <p>visningsprogrammet först läses in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> BANNER  </span> </p> </td> 
   <td colname="col2"> <p>bilden på karusellbanderollen ändras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF  </span> </p> </td> 
   <td colname="col2"> <p>användaren aktiverar hotspot-området. </p> </td> 
  </tr> 
 </tbody> 
</table>
