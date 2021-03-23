---
description: JavaScript API-referens för Video Viewer.
seo-description: JavaScript API-referens för Video Viewer.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
uuid: a4b741a1-b0b3-4bc3-aeab-9d0e44ec4e79
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Video
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# setContainerId{#setcontainerid}

JavaScript API-referens för Video Viewer.

` setContainerId( *`containerId`*)`

Anger ID:t för DOM-behållaren (vanligtvis en `DIV`) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när `init()` körs. Den här parametern anropas före `init()`. Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med JSON-objektet `config` till konstruktorn.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> ID för behållare. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

