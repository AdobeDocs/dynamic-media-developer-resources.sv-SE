---
description: Varnings- eller felinformation för en signeringsuppdatering i en batchSetAssetMetadata-åtgärd.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---

# SetMetadataFault{#setmetadatafault}

Varnings- eller felinformation för en signeringsuppdatering i en batchSetAssetMetadata-åtgärd.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| assetHandle | `xsd:string` | Resursen vars metadata inte kunde anges. |
| fieldHandle | `xsd:string` | Referensen till metadatafältet vars värde inte kunde anges. |
| kod | `xsd:int` | Felkod. |
| orsak | `xsd:string` | Felbeskrivning (oformaterad text). |
