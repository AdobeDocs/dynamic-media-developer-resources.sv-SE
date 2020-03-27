---
description: Sökvägar till bilddatafiler. Anger de filer som innehåller bilddata för den här katalogen.
seo-description: Sökvägar till bilddatafiler. Anger de filer som innehåller bilddata för den här katalogen.
seo-title: CatalogFile
solution: Experience Manager
title: CatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 3599c8d3-dc4b-434e-8b11-775ea6f155ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CatalogFile{#catalogfile}

Sökvägar till bilddatafiler. Anger de filer som innehåller bilddata för den här katalogen.

Bilddatafiler läses in i den angivna ordningen. Om samma `catalog::Id` värde förekommer i mer än en post (antingen i samma eller olika katalogfiler) gäller den sista instansen.

## Egenskaper {#section-6da55f145ecd4e31a5de52637a436983}

Ett eller flera textsträngsvärden, avgränsade med kommatecken. Valfritt. Varje värde måste vara en absolut sökväg eller sökväg i förhållande till katalogmappen.

## Standard {#section-80f91cd7a6b2479ebb310319e9c74da7}

Tom, vilket anger att bildkatalogen inte innehåller bilddata.

## Se även {#section-910b67c5041d44d99a105ad43ff63a37}

[Katalogdatafält](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
