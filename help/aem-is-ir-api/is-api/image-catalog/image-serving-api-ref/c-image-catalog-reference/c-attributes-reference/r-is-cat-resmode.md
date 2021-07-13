---
description: Standardläge för omsampling. Anger de standardattribut för omsampling och interpolation som ska användas för skalning av bilddata.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# ResMode{#resmode}

Standardläge för omsampling. Anger de standardattribut för omsampling och interpolation som ska användas för skalning av bilddata.

Används när `resMode=` inte har angetts i en begäran.

## Egenskaper {#section-493f900be522486f97710cebdc4460c2}

Enum. Ange 2 för interpolationsläget `bilin`, 3 för `bicub` eller 4 för interpolationsläget `sharp2` (mer information finns i ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`). `sharp` (1) har tagits bort. Använd `sharp2` (4) i stället för att få bästa resultat.

## Standard {#section-35f980e745fc4d79a2621e8abacc724d}

Ärvs från `default::ResMode` om det inte är definierat eller om det är tomt.

## Se även {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
