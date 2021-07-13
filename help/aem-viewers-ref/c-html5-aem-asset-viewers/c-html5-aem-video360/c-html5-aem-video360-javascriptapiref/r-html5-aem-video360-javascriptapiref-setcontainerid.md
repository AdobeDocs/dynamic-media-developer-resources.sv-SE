---
description: JavaScript API-referens för Video360 Viewer.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

JavaScript API-referens för Video360 Viewer.

` setContainerId( *`containerId`*)`

Anger ID:t för DOM-behållaren (vanligtvis en DIV) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när `init()` körs. Den måste anropas före `init()`.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med JSON-objektet `config` till konstruktorn.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

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
