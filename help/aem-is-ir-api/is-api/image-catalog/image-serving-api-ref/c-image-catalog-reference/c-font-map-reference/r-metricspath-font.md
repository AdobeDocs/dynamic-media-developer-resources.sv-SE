---
description: Sökväg till teckensnittsmått. Sökväg till och namn på en teckensnittsmåttsfil, inklusive filsuffix.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# MetricsPath{#metricspath}

Sökväg till teckensnittsmått. Sökväg till och namn på en teckensnittsmåttsfil, inklusive filsuffix.

Används för Adobe Type 1-teckensnitt. Om det inte anges försöker servern hitta en teckensnittsmåttsfil i samma mapp som huvudteckensnittsfilen finns i. Ett fel uppstår om en nödvändig teckensnittsmåttsfil inte kan hittas vid återgivningen.

## Egenskaper {#section-955268c581574875b05253d9e14544f3}

Textsträng. Valfritt för Adobe Type 1-filer. Måste vara tom eller ha en giltig sökväg till en Image Server-fil, antingen absolut eller relativ till `attribute::RootPath`.

## Standard {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Ingen.

## Se även {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
