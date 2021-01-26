---
description: Sökresultat för metadata som innehåller sammanfattad information om en resurs.
seo-description: Sökresultat för metadata som innehåller sammanfattad information om en resurs.
seo-title: AssetSummary
solution: Experience Manager
title: AssetSummary
topic: Dynamic Media Image Production System API
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 2%

---


# AssetSummary{#assetsummary}

Sökresultat för metadata som innehåller sammanfattad information om en resurs.

Syntax

## Parametrar {#section-ebc75cc024d94c439260d2e71873cc74}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Resurshandtag. |
| `*`type`*` | `xsd:string` | Resurstyp. Konstanten &quot;Resurstyper&quot; definierar möjliga värden. Valfritt. |
| `*`name`*` | `xsd:string` | Resursnamn. Valfritt. |
| `*`mapp`*` | `xsd:string` | Mappen som innehåller resursen. |
| `*`filnamn`*` | `xsd:string` | Resursens filnamn. |
| `*`skapad`*` | `xsd:dateTime` | Skapad resurs |
| `*`createUser`*` | `xsd:string` | Användaren som skapade resursen. |
| `*`lastModified`*` | `xsd:dateTime` | Det datum då resursen senast uppdaterades. |
| `*`lastModifyUser`*` | `xsd:string` | Den sista användaren som ändrade resursen. |
| `*`metadataArray`*` | `types:MetadataArray` | Array med metadatavärden som är associerade med resursen. |
| `*`score`*` | `xsd:double` | Definierar precisionen vid likhetssökning (0 = ingen matchning, 1 = exakt matchning). |
| `*`scoreDetail`*` | `xsd:string` | Innehåller detaljerad information om liknande områden som ett resultat av en likhetssökning. |

