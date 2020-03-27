---
description: Målet för en klickåtgärd i webbläsaren.
seo-description: Målet för en klickåtgärd i webbläsaren.
seo-title: ImageMap
solution: Experience Manager
title: ImageMap
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageMap{#imagemap}

Målet för en klickåtgärd i webbläsaren.

Alltid associerat med en bild. Du kan hämta ett `ImageMap` mål från `ImageInfo`.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Handtag för bildschema. |
| ` *`name`*` | `xsd:string` | Namn på bildschema. |
| ` *`region`*` | `xsd:string` | Koordinater för bildschema. Format baseras på HTML- `<area>` taggattributet. |
| ` *`åtgärd`*` | `xsd:string` | Andra attribut som ska tas med i HTML- `<area>` taggen, inklusive `href` URL:en. |
| ` *`shapeType`*` | `xsd:boolean` | Ett [!DNL RegionShape] värde. |
| ` *`position`*` | `xsd:string` | Placera i formatet för HTML- `<area>` elementets [!DNL coords] attribut. Exempel: `coords ="0,0,84,128"`. |
| ` *`aktiverad`*` | `xsd:boolean` | True om bildschema är aktiverat. |
| ` *`lastModified`*` | `xsd:dateTime` | Datum och tid då bildschemat senast ändrades. |

