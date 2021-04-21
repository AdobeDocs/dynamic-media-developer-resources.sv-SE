---
description: Returnerar metadatafältdefinitioner för angivna resurstyper.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---


# AssetMetadataFields{#assetmetadatafields}

Returnerar metadatafältdefinitioner för angivna resurstyper.

Syntax

## Parametrar {#section-5ad771540c5f40c187b35e34aac19305}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Resurstyp som är associerad med fältdefinitioner (se &quot;Tillgångstyper&quot; för värden). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Array med metadatafältdefinitioner som är associerade med resurstypen som anges i `assetType`. |

