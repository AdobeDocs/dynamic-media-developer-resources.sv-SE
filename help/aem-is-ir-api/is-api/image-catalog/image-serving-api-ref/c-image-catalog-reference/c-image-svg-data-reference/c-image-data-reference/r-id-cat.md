---
description: Katalogens post-ID
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 7d3902803d42f5d479dd04ac9470a4088809f3d6

---


# ID {#id}

Indexnyckelvärde med vilket poster i bilddatafilen slås upp av plattformsservern.

Vanligtvis är det en kort och unik bildidentifierare, till exempel ett SKU-nummer, eventuellt med någon typ av bildsuffix, om en SKU har flera bilder. Kan också vara en mer komplex sträng som ser mer ut som en filsökväg, som har stöd för enkel återanpassning av webbplatser med Image Serving.

## Egenskaper {#id-properties}

Textsträng. Obligatoriskt. Primär indexnyckel för bilddatatabellen. Varje katalog::Id-värde måste vara unikt i tabellen.

## Standard {#id-default}

Ingen.

## Se även {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)