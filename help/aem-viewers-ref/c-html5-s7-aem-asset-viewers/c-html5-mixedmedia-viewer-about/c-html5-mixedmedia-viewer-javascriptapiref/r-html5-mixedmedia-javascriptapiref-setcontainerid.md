---
description: JavaScript API-referens för blandad Media Viewer.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,Business Practitioner
exl-id: b6e191dc-3172-45ba-b6f6-258cfbd5855d
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

JavaScript API-referens för blandad Media Viewer.

` setContainerId( *`containerId`*)`

Anger ID:t för DOM-behållaren (vanligtvis en DIV) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när `init()` körs. Den måste anropas före `init()`. Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med JSON-objektet `config` till konstruktorn.

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
