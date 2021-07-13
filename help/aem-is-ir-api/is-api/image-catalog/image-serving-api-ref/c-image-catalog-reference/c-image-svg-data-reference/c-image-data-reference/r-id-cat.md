---
description: Katalogens post-ID
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

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
