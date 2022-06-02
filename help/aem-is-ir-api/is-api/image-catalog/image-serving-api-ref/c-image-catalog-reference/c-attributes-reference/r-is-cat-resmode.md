---
title: ResMode
description: Standardläge för omsampling. Anger de standardattribut för omsampling och interpolation som ska användas för skalning av bilddata.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ResMode{#resmode}

Standardläge för omsampling. Anger de standardattribut för omsampling och interpolation som ska användas för skalning av bilddata.

Används när `resMode=` har inte angetts i en begäran.

## Egenskaper {#section-493f900be522486f97710cebdc4460c2}

Enum. Ange 2 för `bilin`, 3 för `bicub`eller 4 för `sharp2` interpolationsläge (se [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) för mer information). `sharp` (1) har tagits bort. Använd `sharp2` (4) i stället för att ge bästa resultat.

## Standard {#section-35f980e745fc4d79a2621e8abacc724d}

Ärvs från `default::ResMode` om den inte är definierad eller om den är tom.

## Se även {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
