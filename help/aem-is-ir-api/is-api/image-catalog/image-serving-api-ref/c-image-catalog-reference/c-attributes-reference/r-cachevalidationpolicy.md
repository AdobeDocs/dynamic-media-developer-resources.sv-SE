---
description: Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
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
