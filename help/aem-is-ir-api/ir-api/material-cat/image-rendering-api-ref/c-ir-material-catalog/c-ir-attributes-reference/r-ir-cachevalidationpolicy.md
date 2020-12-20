---
description: Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.
seo-description: Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Verifieringsprincip för servercache. Anger när cacheposter på serversidan valideras.

Med utgångsbaserad validering kontrolleras källmaterial och vinjetter regelbundet för att se om de har ändrats. Med katalogbaserad validering kontrolleras källbilderna endast efter att `catalog::TimeStamp`-värdet har ändrats.

Katalogbaserad validering rekommenderas när både material- och vinjettkataloger används. Förfallobaserad validering bör användas när vinjetter refereras i begäranden om bildåtergivning direkt via sökväg.

## Egenskaper {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 för att välja förfallobaserad validering. 1 för att välja katalogbaserad cachevalidering.

## Standard {#section-e09f3af8b6b3497d963199988dc5345d}

Ärvs från `default::CacheValidationPolicy` om det inte är definierat eller om det är tomt.

## Se även {#section-b374e4d908e24af8995b2b376ca1be8b}

[katalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
