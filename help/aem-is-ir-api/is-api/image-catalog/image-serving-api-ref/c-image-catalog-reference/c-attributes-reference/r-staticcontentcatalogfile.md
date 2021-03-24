---
description: Sökvägar till datafiler för katalog med statiskt innehåll. Anger de filer som innehåller statiska innehållsdata för den här katalogen.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Sökvägar till datafiler för katalog med statiskt innehåll. Anger de filer som innehåller statiska innehållsdata för den här katalogen.

Datafiler för katalog med statiskt innehåll läses in i den ordning som anges. Om samma `static::Id`-värde förekommer i mer än en post (antingen i samma eller olika katalogfiler) gäller den sista instansen.

## Egenskaper {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Ett eller flera textsträngsvärden, avgränsade med kommatecken. Valfritt. Varje värde måste vara en absolut sökväg eller sökväg i förhållande till katalogmappen.

## Standard {#section-702edfbc00c54fc29e412a3ff99fef2b}

Tom, vilket anger att den här bildkatalogen inte innehåller statiska innehållsdata.

## Se även {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Katalogdata](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
