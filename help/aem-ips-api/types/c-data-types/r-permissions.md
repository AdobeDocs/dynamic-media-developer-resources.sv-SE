---
description: Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.
seo-description: Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.
seo-title: Behörighet
solution: Experience Manager
title: Behörighet
topic: Scene7 Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---


# Behörighet{#permission}

Hanterar behörigheter för åtkomst, ändring, skapande eller borttagning av resurser per grupp.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | Gruppreferens. |
| ` *`groupName`*` | `xsd:string` | Gruppnamn. |
| ` *`permissionType`*` | `xsd:string` | Val av behörighetstyp. |
| ` *`isAllowed`*` | `xsd:boolean` | Anger om behörighet är tillåten. |
| ` *`isOverride`*` | `xsd:boolean` | Avgör om behörigheten åsidosätter en annan. |

