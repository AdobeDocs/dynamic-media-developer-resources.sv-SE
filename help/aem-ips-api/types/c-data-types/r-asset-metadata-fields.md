---
description: Returnerar metadatafältdefinitioner för angivna resurstyper.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Resurshantering
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
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
