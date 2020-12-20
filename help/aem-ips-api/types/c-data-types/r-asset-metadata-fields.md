---
description: Returnerar metadatafältdefinitioner för angivna resurstyper.
seo-description: Returnerar metadatafältdefinitioner för angivna resurstyper.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
topic: Scene7 Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---


# AssetMetadataFields{#assetmetadatafields}

Returnerar metadatafältdefinitioner för angivna resurstyper.

Syntax

## Parametrar {#section-5ad771540c5f40c187b35e34aac19305}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`assetType`*` | `xsd:string` | Resurstyp som är associerad med fältdefinitioner (se &quot;Tillgångstyper&quot; för värden). |
| ` *`fieldArray`*` | `types:MetadataFieldArray` | Array med metadatafältdefinitioner som är associerade med resurstypen som anges i `assetType`. |

