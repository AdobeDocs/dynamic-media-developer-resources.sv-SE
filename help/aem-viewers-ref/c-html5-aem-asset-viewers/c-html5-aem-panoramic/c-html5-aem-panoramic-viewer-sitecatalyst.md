---
title: Stöd för Adobe Analytics tracking
description: Stöd för Adobe Analytics tracking
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Stöd för Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

Som standard skickar visningsprogrammet en enda HTTP-begäran för spårning till konfigurerad Image Server med information om visningsprogramtyp och version.

## Anpassad spårning {#section-cda48fc9730142d0bb3326bac7df3271}

För att kunna integreras med analyssystem från tredje part måste man lyssna på `trackEvent` återanrop och process för visningsprogram `eventInfo` vid behov callback-funktionens argument. Följande kod är ett exempel på en sådan hanterarfunktion:

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
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
   <th colname="col2" class="entry"> <p>Skickat... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LADDA </span> </p> </td> 
   <td colname="col2"> <p>när visningsprogrammet läses in först. </p> </td> 
  </tr> 
 </tbody> 
</table>
