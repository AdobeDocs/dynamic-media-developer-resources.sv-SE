---
description: Katalogens post-ID
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
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