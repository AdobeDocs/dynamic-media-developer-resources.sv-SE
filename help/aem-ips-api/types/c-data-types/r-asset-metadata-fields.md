---
description: Returnerar metadatafältdefinitioner för angivna resurstyper.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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

