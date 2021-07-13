---
description: Bana
solution: Experience Manager
title: Bana
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f273f32-1699-4bc3-8dd0-f1dfefaa6e27
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Bana{#path}

Servern använder de regler för sökvägsupplösning som beskrivs i [Hantera källdata](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) för att hitta datafilen.

## Egenskaper {#section-72d9edc532ad43349afcb4df22e1c692}

Textsträng. Obligatoriskt för bild- och SVG-poster, kan vara tomt för mallposter. Om det anges måste det vara en giltig relativ eller absolut sökväg till Image Server-filen. attribute::DefaultExt läggs till om det inte finns något filsuffix.

## Bildfilformat som stöds {#section-8d6443c883aa48aaa00316fe9661aaa8}

Se beskrivningen av verktyget Image Converter (IC) för en fullständig lista över bildfilformat som stöds.

Program som kräver bilddata i flera olika upplösningar fungerar bäst när du använder multiupplösningsformatet Dynamic Media pyramid TIFF (PTIFF). IC-verktyget används för att skapa PTIFF-bilder från alla bildformat som stöds.

## Standard {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Ingen.

## Se även {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC Utility](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b),  [attribute::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [attribute::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0),  [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
