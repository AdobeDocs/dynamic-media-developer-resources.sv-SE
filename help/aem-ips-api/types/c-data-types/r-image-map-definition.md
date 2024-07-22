---
description: Måldefinition för en klickåtgärd i webbläsaren.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

Måldefinition för en klickåtgärd i webbläsaren.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| name | `xsd:string` | Namnet på definitionen av bildschemat. |
| shapeType | `xsd:string` | Ett av formvärdena för regionen. |
| region | `xsd:string` | Koordinater för bildschema. Formatet baseras på taggattributen för HTML `<area>`. |
| åtgärd | `xsd:string` | Andra attribut som ska inkluderas i taggen `<area>` i HTML, inklusive URL:en `href` . |
| aktiverad | `xsd:boolean` | True if the image map is enabled. |
