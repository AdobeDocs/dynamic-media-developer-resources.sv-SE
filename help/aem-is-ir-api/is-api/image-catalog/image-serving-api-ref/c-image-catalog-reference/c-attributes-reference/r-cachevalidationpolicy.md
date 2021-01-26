---
description: Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.
seo-description: Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 371dadbf-d58e-4214-8050-7e8907b436e3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.

Med förfallobaserad validering kontrolleras källbilderna regelbundet om de har ändrats. Med katalogbaserad validering kontrolleras källbilderna endast efter att `catalog::TimeStamp`-värdet har ändrats.

Katalogbaserad validering rekommenderas när bildkataloger används. Förfallobaserad validering bör användas när bilder refereras direkt, utan användning av en bildkatalog.

## Egenskaper {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 för att välja förfallobaserad validering, 1 för att välja katalogbaserad cachevalidering.

## Standard {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Ärvs från `default::CacheValidationPolicy` om det inte är definierat eller om det är tomt.

## Se även {#section-a0c922fa519641f2bce05e75e4eb51d0}

[katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
