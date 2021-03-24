---
description: Varnings- eller felinformation för en signeringsuppdatering i en batchSetAssetMetadata-åtgärd.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
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

