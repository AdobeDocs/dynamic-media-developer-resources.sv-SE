---
description: Sökväg till bildfil.
solution: Experience Manager
title: Bana
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Bana{#path}

Sökväg till bildfil.

Relativ eller absolut sökväg och namn för källbildfilen som är associerad med den här katalogposten. Servern använder de regler för sökvägsupplösning som beskrivs i Hantera källdata för att hitta datafilen.

## Egenskaper {#path-properties}

Textsträng. Obligatoriskt för bildposter, kan vara tomt för mallposter. Om det anges måste det vara en giltig relativ eller absolut sökväg till Image Server-filen. attribute::DefaultExt läggs till om det inte finns något filsuffix.

## Bildfilformat som stöds {#path-supported-image-file-formats}

Mer information om vilka filformat som stöds finns i beskrivningen av verktyget Image Converter (IC).

Program som kräver bilddata i flera olika upplösningar fungerar bäst när du använder flerupplösningsformatet Dynamic Media pyramid TIFF (PTIFF). IC-verktyget används för att skapa PTIFF-bilder från alla bildformat som stöds.

## Standard {#path-default}

Ingen.

## Se även {#path-seealso}

[Konc.int. verktyg](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
