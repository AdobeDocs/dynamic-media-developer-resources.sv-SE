---
description: Källdatarotsökväg. Absolut eller relativ sökväg för rotmappen för bildkatalogens källdata.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# RootPath{#rootpath}

Källdatarotsökväg. Absolut eller relativ sökväg för rotmappen för bildkatalogens källdata.

The `RootPath` är ett textsträngsvärde. Se [Hantera källdata](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) om du vill ha mer information om serverrotsökvägar.

## Egenskaper {#section-b41d7e0ea63143eb8034569706cad0c0}

Textsträng. Måste vara tom, en giltig relativ mappsökväg eller en giltig absolut sökväg som är tillgänglig för Image Server.

## Standard {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Ärvs från `default::RootPath` om inte definierat. Om den är definierad men tom, kommer inte att bidra till källfilens rotsökväg.

## Se även {#section-6bf4ffc4987843a9a2dbe81b43076437}

[katalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [katalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [linjaluppsättning::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Hantera källdata](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
