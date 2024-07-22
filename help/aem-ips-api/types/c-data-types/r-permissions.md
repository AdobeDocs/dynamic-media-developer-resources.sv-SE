---
description: Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.
solution: Experience Manager
title: Behörighet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---

# [!DNL Permission]{#permission}

Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| groupHandle | `xsd:string` | Grupphandtag. |
| groupName | `xsd:string` | Gruppnamn. |
| permissionType | `xsd:string` | Val av behörighetstyp. |
| isAllowed | `xsd:boolean` | Anger om behörighet är tillåten. |
| isOverride | `xsd:boolean` | Avgör om behörigheten åsidosätter en annan. |
