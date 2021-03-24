---
description: Sökvägar till SVG-datafiler. Anger filerna som innehåller SVG-data för den här katalogen.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# SvgCatalogFile{#svgcatalogfile}

Sökvägar till SVG-datafiler. Anger filerna som innehåller SVG-data för den här katalogen.

SVG-datafiler läses in efter alla bilddatafiler i exakt angiven ordning. Om samma `catalog::Id`-värde förekommer i mer än en post (antingen i samma eller en annan bild eller i SVG-katalogfiler) gäller den sista instansen.

## Egenskaper {#section-fc2d549f76474792837b2b92ec2087ea}

Ett eller flera textsträngsvärden, avgränsade med kommatecken. Valfritt. Varje värde måste vara en absolut sökväg eller sökväg i förhållande till katalogmappen.

## Standard {#section-a4e58951f3c249599665b823566433c9}

Tom, vilket betyder att den här bildkatalogen inte innehåller SVG-data.

## Se även {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Katalogdata](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29),  [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
