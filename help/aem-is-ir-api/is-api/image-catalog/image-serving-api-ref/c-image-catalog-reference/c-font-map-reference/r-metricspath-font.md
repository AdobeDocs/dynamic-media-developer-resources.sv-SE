---
description: Sökväg till teckensnittsmått. Sökväg till och namn på en teckensnittsmåttsfil, inklusive filsuffix.
seo-description: Sökväg till teckensnittsmått. Sökväg till och namn på en teckensnittsmåttsfil, inklusive filsuffix.
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
topic: Scene7 Image Serving - Image Rendering API
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# MetricsPath{#metricspath}

Sökväg till teckensnittsmått. Sökväg till och namn på en teckensnittsmåttsfil, inklusive filsuffix.

Används för Adobe Type 1-teckensnitt. Om det inte anges försöker servern hitta en teckensnittsmåttsfil i samma mapp som huvudteckensnittsfilen finns i. Ett fel uppstår om en nödvändig teckensnittsmåttsfil inte kan hittas vid återgivningen.

## Egenskaper {#section-955268c581574875b05253d9e14544f3}

Textsträng. Valfritt för Adobe Type 1-filer. Måste vara tom eller en giltig sökväg till en Image Server-fil, antingen absolut eller relativ till `attribute::RootPath`.

## Standard {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Ingen.

## Se även {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
