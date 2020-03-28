---
description: JavaScript API-referens för eCatalog Viewer.
seo-description: JavaScript API-referens för eCatalog Viewer.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 19149e38-b9d2-4ecd-a555-92e2960f7ee3
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setContainerId{#setcontainerid}

JavaScript API-referens för eCatalog Viewer.

[!DNL ` setContainerId( *`containerId`*)`]

Anger ID:t för [!DNL `DOM` -behållaren (vanligtvis en [!DNL `DIV`]) som visningsprogrammet infogas i. Det är inte nödvändigt att ha behållarelementet skapat när metoden anropas. Behållaren måste dock finnas när [!DNL `init()`] den körs. Den måste anropas innan [!DNL `init()`].

Den här metoden är valfri om visningsprogrammets konfigurationsinformation skickas med [!DNL `config`] JSON-objektet till konstruktorn.

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

