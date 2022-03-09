---
description: Jobblogginformation.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# JobLogDetail{#joblogdetail}

Jobblogginformation.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| logMessage | `xsd:string` | Meddelanden i jobbloggen. |
| logType | `xsd:string` | Filtyp för jobblogg. |
| assetName | `xsd:string` | Namnet på resursen i jobbloggen (valfritt). |
| assetType | `xsd:string` | Val av resurstyp. |
| assetHandle | `xsd:string` | Resurshandtag som refereras i jobbloggen. |
| auxArray | `types:JobLogDetailAuxArray` | Innehåller ytterligare detaljerad jobblogginformation utöver de fem jobbloggtyperna som beskrivs ovan. |
