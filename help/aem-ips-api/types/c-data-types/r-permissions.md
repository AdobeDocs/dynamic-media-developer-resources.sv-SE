---
description: Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.
solution: Experience Manager
title: Behörighet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# Behörighet{#permission}

Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| groupHandle | `xsd:string` | Gruppreferens. |
| groupName | `xsd:string` | Gruppnamn. |
| permissionType | `xsd:string` | Val av behörighetstyp. |
| isAllowed | `xsd:boolean` | Anger om behörighet är tillåten. |
| isOverride | `xsd:boolean` | Avgör om behörigheten åsidosätter en annan. |
