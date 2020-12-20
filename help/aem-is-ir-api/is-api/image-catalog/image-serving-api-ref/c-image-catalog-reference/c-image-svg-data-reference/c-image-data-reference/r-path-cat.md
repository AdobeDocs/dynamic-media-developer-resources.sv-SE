---
description: Sökväg till bildfil.
solution: Experience Manager
title: Bana
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 7b837020deef888a038a074d0aa826d43e60aeb6
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Sökväg{#path}

Sökväg till bildfil.

Relativ eller absolut sökväg och namn för källbildfilen som är associerad med den här katalogposten. Servern använder de regler för sökvägsupplösning som beskrivs i Hantera källdata för att hitta datafilen.

## Egenskaper {#path-properties}

Textsträng. Obligatoriskt för bildposter, kan vara tomt för mallposter. Om det anges måste det vara en giltig relativ eller absolut sökväg till Image Server-filen. attribute::DefaultExt läggs till om det inte finns något filsuffix.

## Bildfilformat som stöds {#path-supported-image-file-formats}

Mer information om vilka filformat som stöds finns i beskrivningen av verktyget Image Converter (IC).

Program som kräver bilddata i flera olika upplösningar fungerar bäst när du använder multiupplösningsformatet Dynamic Media pyramid TIFF (PTIFF). IC-verktyget används för att skapa PTIFF-bilder från alla bildformat som stöds.

## Standard {#path-default}

Ingen.

## Se även {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->