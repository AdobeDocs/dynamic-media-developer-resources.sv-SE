---
description: Målet för en klickåtgärd i webbläsaren.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# ImageMap{#imagemap}

Målet för en klickåtgärd i webbläsaren.

Alltid associerat med en bild. Du kan få en `ImageMap` mål från `ImageInfo`.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| imageMapHandle | `xsd:string` | Handtag för bildschema. |
| name | `xsd:string` | Namn på bildschema. |
| region | `xsd:string` | Koordinater för bildschema. Formatet baseras på HTML `<area>` taggattribut. |
| åtgärd | `xsd:string` | Andra attribut att inkludera i HTML `<area>` -taggen, inklusive `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] värde. |
| position | `xsd:string` | Position i formatet HTML `<area>` element [!DNL coords] -attribut. Exempel: `coords ="0,0,84,128"`. |
| aktiverad | `xsd:boolean` | True om bildschema är aktiverat. |
| lastModified | `xsd:dateTime` | Datum och tid då bildschemat senast ändrades. |
