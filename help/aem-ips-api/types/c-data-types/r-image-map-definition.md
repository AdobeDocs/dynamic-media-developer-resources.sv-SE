---
description: Måldefinition för en klickåtgärd i webbläsaren.
seo-description: Måldefinition för en klickåtgärd i webbläsaren.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Dynamic Media Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 1%

---


# ImageMapDefinition{#imagemapdefinition}

Måldefinition för en klickåtgärd i webbläsaren.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`name`*` | `xsd:string` | Namnet på definitionen av bildschemat. |
| `*`shapeType`*` | `xsd:string` | Ett av formvärdena för regionen. |
| `*`region`*` | `xsd:string` | Koordinater för bildschema. Formatet baseras på HTML-taggattributen `<area>`. |
| `*`åtgärd`*` | `xsd:string` | Andra attribut som ska tas med i HTML-taggen `<area>`, inklusive URL:en `href`. |
| `*`aktiverad`*` | `xsd:boolean` | True om bildschemat är aktiverat. |

