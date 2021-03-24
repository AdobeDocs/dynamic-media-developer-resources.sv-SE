---
description: Måldefinition för en klickåtgärd i webbläsaren.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
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

