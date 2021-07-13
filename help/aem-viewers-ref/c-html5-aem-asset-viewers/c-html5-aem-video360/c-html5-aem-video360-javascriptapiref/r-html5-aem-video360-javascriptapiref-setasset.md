---
description: JavaScript API-referens för Video360 Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video
role: Developer,User
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referens för Video360 Viewer.

`setAsset(asset)`

Anger den nya resursen. Du kan anropa den här parametern när som helst, antingen före eller efter `init()`. Om det anropas efter `init()` byter visningsprogrammet resursen under körning.

Se även [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> resurs  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Sträng</span>} nytt resurs-ID. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Viewers/space_station_360-AVS")
```
