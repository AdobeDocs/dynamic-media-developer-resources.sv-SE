---
description: Måldefinition för en klickåtgärd i webbläsaren.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---

# ImageMapDefinition{#imagemapdefinition}

Måldefinition för en klickåtgärd i webbläsaren.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| name | `xsd:string` | Namnet på definitionen av bildschemat. |
| shapeType | `xsd:string` | Ett av formvärdena för regionen. |
| region | `xsd:string` | Koordinater för bildschema. Formatet baseras på HTML `<area>` taggattribut. |
| åtgärd | `xsd:string` | Andra attribut att inkludera i HTML `<area>` -taggen, inklusive `href` URL. |
| aktiverad | `xsd:boolean` | True om bildschemat är aktiverat. |
