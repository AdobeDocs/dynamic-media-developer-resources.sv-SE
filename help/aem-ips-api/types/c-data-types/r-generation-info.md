---
description: PostScript-filegenskaper.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 0%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScript-filegenskaper.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| [!DNL engine] | `xsd:string` | Genereringsmotor som används (se&quot;Generationsinformation&quot; för värden). |
| [!DNL originator] | `types:Asset` | Tillgångspost för den primära tillgång som används i genereringen. |
| [!DNL generated] | `types:Asset` | Tillgångspost för den genererade resursen. |
| attributeArray | `types:GenerationAttributeArray` | Array med attribut som är associerade med genereringsprocessen. |
