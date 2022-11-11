---
description: Målet för en klickåtgärd i webbläsaren.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---

# [!DNL ImageMap]{#imagemap}

Målet för en klickåtgärd i webbläsaren.

Alltid associerat med en bild. Du kan få en `ImageMap` mål från `ImageInfo`.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| imageMapHandle | `xsd:string` | Handtag för bildschema. |
| [!DNL name] | `xsd:string` | Namn på bildschema. |
| [!DNL region] | `xsd:string` | Koordinater för bildschema. Formatet baseras på HTML `<area>` taggattribut. |
| [!DNL action] | `xsd:string` | Andra attribut att inkludera i HTML `<area>` -taggen, inklusive `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] värde. |
| [!DNL position] | `xsd:string` | Position i formatet HTML `<area>` element [!DNL coords] -attribut. Exempel: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True om bildschema är aktiverat. |
| lastModified | `xsd:dateTime` | Datum och tid då bildschemat senast ändrades. |
