---
description: Katalogens post-ID
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# ID {#id}

Indexnyckelvärde som poster i bilddatafilen slås upp med [!DNL Platform Server].

Vanligtvis är det en kort och unik bildidentifierare, till exempel ett SKU-nummer, eventuellt med någon typ av bildsuffix, om en SKU har flera bilder. Kan också vara en mer komplex sträng som ser mer ut som en filsökväg, som har stöd för enkel återanpassning av webbplatser med Image Serving.

## Egenskaper {#id-properties}

Textsträng. Obligatoriskt. Primär indexnyckel för bilddatatabellen. Varje katalog::Id-värde måste vara unikt i tabellen.

## Standard {#id-default}

Ingen.

## Se även {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
