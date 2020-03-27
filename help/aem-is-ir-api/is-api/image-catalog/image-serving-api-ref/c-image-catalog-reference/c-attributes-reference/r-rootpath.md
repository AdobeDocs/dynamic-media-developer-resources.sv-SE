---
description: Källdatarotsökväg. Absolut eller relativ sökväg för rotmappen för bildkatalogens källdata.
seo-description: Källdatarotsökväg. Absolut eller relativ sökväg för rotmappen för bildkatalogens källdata.
seo-title: RootPath
solution: Experience Manager
title: RootPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 859bebf2-5ee7-4daa-8970-a18bddcee684
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# RootPath{#rootpath}

Källdatarotsökväg. Absolut eller relativ sökväg för rotmappen för bildkatalogens källdata.

Värdet `RootPath` är ett textsträngsvärde. Mer information om serverrotsökvägar finns i [Hantera källdata](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) .

## Egenskaper {#section-b41d7e0ea63143eb8034569706cad0c0}

Textsträng. Måste vara tom, en giltig relativ mappsökväg eller en giltig absolut sökväg som är tillgänglig för Image Server.

## Standard {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Ärvs från `default::RootPath` om inte definierat. Om den är definierad men tom, kommer inte att bidra till källfilens rotsökväg.

## Se även {#section-6bf4ffc4987843a9a2dbe81b43076437}

[katalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [katalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [regeluppsättning::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [hantera källdata](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
