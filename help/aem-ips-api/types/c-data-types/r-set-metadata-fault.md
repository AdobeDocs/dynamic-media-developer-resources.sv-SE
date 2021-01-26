---
description: Varnings- eller felinformation för en signeringsuppdatering i en batchSetAssetMetadata-åtgärd.
seo-description: Varnings- eller felinformation för en signeringsuppdatering i en batchSetAssetMetadata-åtgärd.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Dynamic Media Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# SetMetadataFault{#setmetadatafault}

Varnings- eller felinformation för en signeringsuppdatering i en batchSetAssetMetadata-åtgärd.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Resursen vars metadata inte kunde anges. |
| `*`fieldHandle`*` | `xsd:string` | Referensen till metadatafältet vars värde inte kunde anges. |
| `*`kod`*` | `xsd:int` | Felkod. |
| `*`orsak`*` | `xsd:string` | Felbeskrivning (oformaterad text). |

