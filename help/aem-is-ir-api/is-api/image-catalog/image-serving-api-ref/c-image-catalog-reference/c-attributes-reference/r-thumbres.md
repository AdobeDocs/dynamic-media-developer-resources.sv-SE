---
description: Standardupplösning för miniatyrbilder. Anger ett standardvärde för upplösningen av miniatyrbildobjektet om en viss katalogpost inte innehåller ett giltigt ThumbRes-katalogvärde.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# ThumbRes{#thumbres}

Standardupplösning för miniatyrbilder. Anger en standardinställning för upplösningen av miniatyrbildobjektet om en viss katalogpost inte innehåller ett giltigt katalogvärde::ThumbRes-värde.

Används endast för miniatyrbegäranden ( `req=tmb`) och när `catalog::ThumbType=3`.

## Egenskaper {#section-88d37d0e030f4879a9e584dd2cc780f3}

Reellt tal som är större än 0. Uttryckt som pixlar per tum, men kan också finnas i andra enheter, t.ex. pixlar per meter.

## Standard {#section-86588899ec9b4276a98b03d7faf64003}

Ärvs från `default::ThumbRes` om det inte är definierat eller om det är tomt.

## Se även {#section-a6d2cce2e404441a996dba98a95c8e16}

[katalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
