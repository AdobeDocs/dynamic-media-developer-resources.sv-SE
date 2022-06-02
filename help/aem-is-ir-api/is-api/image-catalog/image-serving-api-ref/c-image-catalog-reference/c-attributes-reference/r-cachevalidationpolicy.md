---
title: CacheValidationPolicy
description: Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.

Med förfallobaserad validering kontrolleras källbilderna regelbundet om de har ändrats. Med katalogbaserad validering kontrolleras källbilderna endast efter `catalog::TimeStamp` värdet har ändrats.

Katalogbaserad validering rekommenderas när bildkataloger används. Förfallobaserad validering bör användas när bilder refereras direkt, utan användning av en bildkatalog.

## Egenskaper {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 för att välja förfallobaserad validering, 1 för att välja katalogbaserad cachevalidering.

## Standard {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Ärvs från `default::CacheValidationPolicy` om den inte är definierad eller om den är tom.

## Se även {#section-a0c922fa519641f2bce05e75e4eb51d0}

[katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
