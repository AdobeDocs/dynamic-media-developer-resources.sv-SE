---
description: JavaScript API-referens för Spin Viewer.
seo-description: JavaScript API-referens för Spin Viewer.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 6ed57f8f-5a5e-4dfa-9ab5-0f724603a0bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

JavaScript API-referens för Spin Viewer.

` setContainerId( *`containerId`*)`

Anger ID:t för DOM-behållaren (vanligtvis en DIV) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när `init()` den körs. Den måste anropas innan `init()`.

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med `config` JSON-objektet till konstruktorn.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> -ID för behållare. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ingen.

## Exempel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

