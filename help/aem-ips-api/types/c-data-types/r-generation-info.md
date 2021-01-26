---
description: PostScript-filegenskaper.
seo-description: PostScript-filegenskaper.
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
topic: Dynamic Media Image Production System API
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---


# GenerationInfo{#generationinfo}

PostScript-filegenskaper.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`motor`*` | `xsd:string` | Genereringsmotor som används (se&quot;Generationsinformation&quot; för värden). |
| `*`upphovsman`*` | `types:Asset` | Tillgångspost för den primära tillgång som används i genereringen. |
| `*`genererad`*` | `types:Asset` | Tillgångspost för den genererade resursen. |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | Array med attribut som är associerade med genereringsprocessen. |

