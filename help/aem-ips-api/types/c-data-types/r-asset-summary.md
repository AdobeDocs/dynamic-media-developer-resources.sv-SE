---
description: Sökresultat för metadata som innehåller sammanfattad information om en resurs.
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# AssetSummary{#assetsummary}

Sökresultat för metadata som innehåller sammanfattad information om en resurs.

Syntax

## Parametrar {#section-ebc75cc024d94c439260d2e71873cc74}

| Namn | Typ | Beskrivning |
|---|---|---|
| assetHandle | `xsd:string` | Resurshandtag. |
| type | `xsd:string` | Resurstyp. Konstanten &quot;Resurstyper&quot; definierar möjliga värden. Valfritt. |
| name | `xsd:string` | Resursnamn. Valfritt. |
| mapp | `xsd:string` | Mappen som innehåller resursen. |
| filnamn | `xsd:string` | Resursens filnamn. |
| skapad | `xsd:dateTime` | Skapad resurs |
| createUser | `xsd:string` | Användaren som skapade resursen. |
| lastModified | `xsd:dateTime` | Det datum då resursen senast uppdaterades. |
| lastModifyUser | `xsd:string` | Den sista användaren som ändrade resursen. |
| metadataArray | `types:MetadataArray` | Array med metadatavärden som är associerade med resursen. |
| score | `xsd:double` | Definierar precisionen vid likhetssökning (0 = ingen matchning, 1 = exakt matchning). |
| scoreDetail | `xsd:string` | Innehåller detaljerad information om liknande områden som ett resultat av en likhetssökning. |
