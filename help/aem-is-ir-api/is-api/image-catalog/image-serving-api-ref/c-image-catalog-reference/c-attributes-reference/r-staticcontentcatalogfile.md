---
description: Sökvägar till datafiler för katalog med statiskt innehåll. Anger de filer som innehåller statiska innehållsdata för den här katalogen.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

Sökvägar till datafiler för katalog med statiskt innehåll. Anger de filer som innehåller statiska innehållsdata för den här katalogen.

Datafiler för katalog med statiskt innehåll läses in i den ordning som anges. Om samma `static::Id` värdet finns i mer än en post (antingen i samma eller olika katalogfiler), gäller den sista instansen.

## Egenskaper {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Ett eller flera textsträngsvärden, avgränsade med kommatecken. Valfritt. Varje värde måste vara en absolut sökväg eller sökväg i förhållande till katalogmappen.

## Standard {#section-702edfbc00c54fc29e412a3ff99fef2b}

Tom, vilket anger att den här bildkatalogen inte innehåller statiska innehållsdata.

## Se även {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Katalogdata](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
