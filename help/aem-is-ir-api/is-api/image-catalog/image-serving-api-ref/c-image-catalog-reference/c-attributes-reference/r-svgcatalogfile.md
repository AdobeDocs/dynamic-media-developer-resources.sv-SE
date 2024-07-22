---
description: Sökvägar till datafiler i SVG. Anger de filer som innehåller SVG-data för den här katalogen.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# SvgCatalogFile{#svgcatalogfile}

Sökvägar till datafiler i SVG. Anger de filer som innehåller SVG-data för den här katalogen.

datafiler i SVG läses in efter alla bilddatafiler i exakt angiven ordning. Om samma `catalog::Id`-värde förekommer i mer än en post (antingen i samma eller olika bild- eller SVG-katalogfiler) gäller den sista instansen.

## Egenskaper {#section-fc2d549f76474792837b2b92ec2087ea}

Ett eller flera textsträngsvärden, avgränsade med kommatecken. Valfritt. Varje värde måste vara en absolut sökväg eller sökväg i förhållande till katalogmappen.

## Standard {#section-a4e58951f3c249599665b823566433c9}

Tomt, vilket anger att bildkatalogen inte innehåller några SVG-data.

## Se även {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Katalogdata](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
