---
description: Sökväg till bildfil. Relativ sökväg och namn för en textur- eller dekal bildfil.
seo-description: Sökväg till bildfil. Relativ sökväg och namn för en textur- eller dekal bildfil.
seo-title: Bana *
solution: Experience Manager
title: Bana *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9e85a358-3f2f-4b8b-a98f-03de2a1a8a4c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# Sökväg *{#path}

Sökväg till bildfil. Relativ sökväg och namn för en textur- eller dekal bildfil.

Servern kombinerar det här värdet med `attribute::RootPath` för att skapa den faktiska sökvägen till bildfilen. Kan också vara en absolut sökväg.

Används för att ange texturbildfilen för textur-, skåp- och fönsterövertäckningsmaterial samt RGB- eller RGBA-bildfilen för dekalt- och väggkantmaterial. Alla kabinett- och fönsterbeläggningsmaterial kräver inte en separat repeterbar texturbild.

## Egenskaper {#section-8c12ea24f21d4472be677581893e6681}

Textsträng. Krävs för textur- och dekmaterial, valfritt för skåp och fönsterbeläggningsmaterial. Om det anges måste det vara en giltig relativ eller absolut filsökväg. Måste vara tomt för heltäckande färgmaterial.

## Filformat som stöds {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Bildåtergivning stöder samma källbildformat som Dynamic Media Image Serving.

Program som kräver bilddata i flera olika upplösningar fungerar bäst när du använder multiupplösningsformatet Dynamic Media pyramid TIFF (PTIFF). Image Serving innehåller verktyget Image Converter (IC) som skapar PTIFF-bilder i alla format som stöds.

Se beskrivningen av verktyget IC i dokumentationen för Image Serving för en fullständig lista över filformat som stöds.

## Standard {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Ingen.

## Se även {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [attribute::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
