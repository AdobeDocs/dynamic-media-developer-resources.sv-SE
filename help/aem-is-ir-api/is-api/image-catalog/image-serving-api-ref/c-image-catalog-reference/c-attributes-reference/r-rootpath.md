---
description: Source datarotsökväg. Absolut eller relativ sökväg för rotmappen för den här bildkatalogens källdata.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# RootPath{#rootpath}

Source datarotsökväg. Absolut eller relativ sökväg för rotmappen för den här bildkatalogens källdata.

`RootPath` är ett textsträngsvärde. Mer information om serverrotsökvägar finns i [Hantera Source-data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e).

## Egenskaper {#section-b41d7e0ea63143eb8034569706cad0c0}

Textsträng. Måste vara tom, en giltig relativ mappsökväg eller en giltig absolut sökväg som är tillgänglig för Image Server.

## Standard {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Ärvs från `default::RootPath` om inte definierat. Om den är definierad men tom, bidrar den inte till källfilens rotsökväg.

## Se även {#section-6bf4ffc4987843a9a2dbe81b43076437}

[katalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [katalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [regeluppsättning::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Hantera Source-data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
