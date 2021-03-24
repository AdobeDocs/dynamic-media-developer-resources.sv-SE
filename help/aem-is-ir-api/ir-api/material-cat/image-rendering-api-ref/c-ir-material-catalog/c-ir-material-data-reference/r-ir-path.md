---
description: Sökväg till bildfil. Relativ sökväg och namn för en textur- eller dekal bildfil.
solution: Experience Manager
title: Bana *
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
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
