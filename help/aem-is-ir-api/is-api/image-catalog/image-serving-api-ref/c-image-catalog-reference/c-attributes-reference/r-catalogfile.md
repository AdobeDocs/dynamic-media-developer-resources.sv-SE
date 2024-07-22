---
description: Sökvägar till bilddatafiler. Anger de filer som innehåller bilddata för den här katalogen.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# CatalogFile{#catalogfile}

Sökvägar till bilddatafiler. Anger de filer som innehåller bilddata för den här katalogen.

Bilddatafiler läses in i den angivna ordningen. Om samma `catalog::Id`-värde förekommer i mer än en post (antingen i samma eller olika katalogfiler) gäller den sista instansen.

## Egenskaper {#section-6da55f145ecd4e31a5de52637a436983}

Ett eller flera textsträngsvärden, avgränsade med kommatecken. Valfritt. Varje värde måste vara en absolut sökväg eller sökväg i förhållande till katalogmappen.

## Standard {#section-80f91cd7a6b2479ebb310319e9c74da7}

Tom, vilket anger att bildkatalogen inte innehåller bilddata.

## Se även {#section-910b67c5041d44d99a105ad43ff63a37}

[Katalogdatafält](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
