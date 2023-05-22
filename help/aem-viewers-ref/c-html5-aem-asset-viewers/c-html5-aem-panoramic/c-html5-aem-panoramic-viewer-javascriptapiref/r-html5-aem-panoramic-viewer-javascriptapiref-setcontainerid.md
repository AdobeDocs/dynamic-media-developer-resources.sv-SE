---
title: setContainerId
description: JavaScript API-referens för panoramavisningsprogrammet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

JavaScript API-referens för panoramavisningsprogrammet.

` setContainerId( *`containerId`*)`

Anger ID:t för DOM-behållaren (vanligtvis en DIV) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när `init()` körs. Den måste anropas före `init()`.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med `config` JSON-objekt till konstruktorn.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID för behållare. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
