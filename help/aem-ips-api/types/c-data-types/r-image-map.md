---
description: Målet för en klickåtgärd i webbläsaren.
seo-description: Målet för en klickåtgärd i webbläsaren.
seo-title: ImageMap
solution: Experience Manager
title: ImageMap
topic: Dynamic Media Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# ImageMap{#imagemap}

Målet för en klickåtgärd i webbläsaren.

Alltid associerat med en bild. Du kan hämta ett `ImageMap`-mål från `ImageInfo`.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Handtag för bildschema. |
| `*`name`*` | `xsd:string` | Namn på bildschema. |
| `*`region`*` | `xsd:string` | Koordinater för bildschema. Formatet baseras på HTML-taggattributet `<area>`. |
| `*`åtgärd`*` | `xsd:string` | Andra attribut som ska tas med i HTML-taggen `<area>`, inklusive URL:en `href`. |
| `*`shapeType`*` | `xsd:boolean` | Ett [!DNL RegionShape]-värde. |
| `*`position`*` | `xsd:string` | Placera i formatet för HTML-elementets `<area>`-attribut. [!DNL coords] Exempel: `coords ="0,0,84,128"`. |
| `*`aktiverad`*` | `xsd:boolean` | True om bildschema är aktiverat. |
| `*`lastModified`*` | `xsd:dateTime` | Datum och tid då bildschemat senast ändrades. |

