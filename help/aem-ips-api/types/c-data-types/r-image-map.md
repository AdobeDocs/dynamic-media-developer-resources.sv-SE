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
ht-degree: 0%

---

# [!DNL ImageMap]{#imagemap}

Målet för en klickåtgärd i webbläsaren.

Alltid associerat med en bild. Du kan hämta ett `ImageMap`-mål från `ImageInfo`.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| imageMapHandle | `xsd:string` | Bildkartans handtag. |
| [!DNL name] | `xsd:string` | Namn på bildschema |
| [!DNL region] | `xsd:string` | Koordinater för bildschema. Formatet baseras på taggattributet `<area>` i HTML. |
| [!DNL action] | `xsd:string` | Andra attribut som ska inkluderas i taggen `<area>` i HTML, inklusive URL:en `href` . |
| shapeType | `xsd:boolean` | Värdet [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Placera i formatet för HTML `<area>`-elementets [!DNL coords]-attribut. Till exempel: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True om bildschema är aktiverat. |
| lastModified | `xsd:dateTime` | Datum och tid då bildschemat senast ändrades. |
