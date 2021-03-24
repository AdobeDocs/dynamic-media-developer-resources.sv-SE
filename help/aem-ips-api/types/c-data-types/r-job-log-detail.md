---
description: Jobblogginformation.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# JobLogDetail{#joblogdetail}

Jobblogginformation.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Meddelanden i jobbloggen. |
| `*`logType`*` | `xsd:string` | Filtyp för jobblogg. |
| `*`assetName`*` | `xsd:string` | Namnet på resursen i jobbloggen (valfritt). |
| `*`assetType`*` | `xsd:string` | Val av resurstyp. |
| `*`assetHandle`*` | `xsd:string` | Resurshandtag som refereras i jobbloggen. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | Innehåller ytterligare detaljerad jobblogginformation utöver de fem jobbloggtyperna som beskrivs ovan. |

