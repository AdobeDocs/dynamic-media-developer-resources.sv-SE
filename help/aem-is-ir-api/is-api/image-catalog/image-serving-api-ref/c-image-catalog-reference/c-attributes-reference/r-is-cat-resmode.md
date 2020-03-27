---
description: Standardläge för omsampling. Anger de standardattribut för omsampling och interpolation som ska användas för skalning av bilddata.
seo-description: Standardläge för omsampling. Anger de standardattribut för omsampling och interpolation som ska användas för skalning av bilddata.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ResMode{#resmode}

Standardläge för omsampling. Anger de standardattribut för omsampling och interpolation som ska användas för skalning av bilddata.

Används när `resMode=` inte anges i en begäran.

## Egenskaper {#section-493f900be522486f97710cebdc4460c2}

Enum. Ange 2 för `bilin`, 3 för `bicub`eller 4 för `sharp2` interpolationsläge (se ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` för mer information). `sharp` (1) har tagits bort. Använd `sharp2` (4) istället för att få bästa resultat.

## Standard {#section-35f980e745fc4d79a2621e8abacc724d}

Ärvs från `default::ResMode` om inte definierad eller om tom.

## Se även {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
