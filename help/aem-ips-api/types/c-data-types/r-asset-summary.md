---
description: Sökresultat för metadata som innehåller sammanfattad information om en resurs.
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
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

