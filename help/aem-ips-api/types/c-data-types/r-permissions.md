---
description: Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.
solution: Experience Manager
title: Behörighet
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---


# Behörighet{#permission}

Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Gruppreferens. |
| `*`groupName`*` | `xsd:string` | Gruppnamn. |
| `*`permissionType`*` | `xsd:string` | Val av behörighetstyp. |
| `*`isAllowed`*` | `xsd:boolean` | Anger om behörighet är tillåten. |
| `*`isOverride`*` | `xsd:boolean` | Avgör om behörigheten åsidosätter en annan. |

