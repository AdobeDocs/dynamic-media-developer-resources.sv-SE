---
description: Söksträngspost som har extraherats från en PDF-fil.
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# [!DNL SearchStrings]{#searchstrings}

Söksträngspost som har extraherats från en PDF-fil.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| searchString | `xsd:string` | Söksträngstext. |
| keywordsArray | `types:KeywordsArray` | En array med nyckelord i söksträngen. |
| status | `xsd:boolean` | True if the search string is valid and enabled. |
| x | `xsd:int` | Söksträngens X-axelposition. |
| y | `xsd:int` | Söksträngens Y-axelposition. |
| width | `xsd:int` | Söksträngsbredd. |
| height | `xsd:int` | Söksträngens höjd. |
| fontName | `xsd:string` | Namnet på det teckensnitt som används i söksträngen. |
| pointSize | `xsd:string` | Teckenstorlek. |
