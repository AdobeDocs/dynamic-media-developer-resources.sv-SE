---
description: Sökvägar till SVG-datafiler. Anger filerna som innehåller SVG-data för den här katalogen.
seo-description: Sökvägar till SVG-datafiler. Anger filerna som innehåller SVG-data för den här katalogen.
seo-title: SvgCatalogFile
solution: Experience Manager
title: SvgCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SvgCatalogFile{#svgcatalogfile}

Sökvägar till SVG-datafiler. Anger filerna som innehåller SVG-data för den här katalogen.

SVG-datafiler läses in efter alla bilddatafiler i exakt angiven ordning. Om samma `catalog::Id` värde förekommer i mer än en post (antingen i samma eller en annan bild eller i SVG-katalogfiler) gäller den sista instansen.

## Egenskaper {#section-fc2d549f76474792837b2b92ec2087ea}

Ett eller flera textsträngsvärden, avgränsade med kommatecken. Valfritt. Varje värde måste vara en absolut sökväg eller sökväg i förhållande till katalogmappen.

## Standard {#section-a4e58951f3c249599665b823566433c9}

Tom, vilket betyder att den här bildkatalogen inte innehåller SVG-data.

## Se även {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Katalogdata](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
