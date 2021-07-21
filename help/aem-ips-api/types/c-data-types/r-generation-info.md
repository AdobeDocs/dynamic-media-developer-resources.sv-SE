---
description: PostScript-filegenskaper.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '54'
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
