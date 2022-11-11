---
description: Ett metadatafält som returneras av searchAssets.
solution: Experience Manager
title: Metadata
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# [!DNL Metadata]{#metadata}

Ett metadatafält som returneras av searchAssets.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| name | `xsd:string` | Metadatanamn. |
| value | `xsd:string` | Metadatavärde. |
| boolVal | `xsd:boolean` | Booleskt metadatavärde (endast för fält av typen Boolean). |
| longVal | `xsd:long` | Långt metadatavärde (endast för fält av typen int). |
| doubleVal | `xsd:double` | Dubbelt metadatavärde (endast för fält med flyttal). |
| dateVal | `xsd:dateTime` | Datummetadatavärde (endast för datumtypsfält). |
