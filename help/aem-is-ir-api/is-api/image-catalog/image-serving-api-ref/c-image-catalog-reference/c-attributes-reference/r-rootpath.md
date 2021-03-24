---
description: Källdatarotsökväg. Absolut eller relativ sökväg för rotmappen för bildkatalogens källdata.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# RootPath{#rootpath}

Källdatarotsökväg. Absolut eller relativ sökväg för rotmappen för bildkatalogens källdata.

`RootPath` är ett textsträngsvärde. Mer information om serverrotsökvägar finns i [Hantera källdata](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e).

## Egenskaper {#section-b41d7e0ea63143eb8034569706cad0c0}

Textsträng. Måste vara tom, en giltig relativ mappsökväg eller en giltig absolut sökväg som är tillgänglig för Image Server.

## Standard {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Ärvs från `default::RootPath` om inte definierat. Om den är definierad men tom, kommer inte att bidra till källfilens rotsökväg.

## Se även {#section-6bf4ffc4987843a9a2dbe81b43076437}

[katalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [katalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),   [regeluppsättning::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [hantera källdata](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
