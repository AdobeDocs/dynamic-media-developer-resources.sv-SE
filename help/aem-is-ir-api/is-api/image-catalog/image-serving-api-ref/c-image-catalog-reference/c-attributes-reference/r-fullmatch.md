---
description: Katalogmatchningsalternativ.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# FullMatch{#fullmatch}

Katalogmatchningsalternativ.

En katalogpost anges som `*`rootId`*/ *`imageId`*` i HTTP-begäranden. Vid tolkning väljs en katalog om `*`rootId`*` matchar `attribute::RootId` värdet för katalogen och katalogposten identifieras genom matchning `*`imageId`*` med `catalog::Id` värde. Om en katalog hittas, men det inte finns någon matchning av katalogposter `*`imageId`*`kan servern göra något av två saker:

If `attribute::FullMatch` har inte angetts, används attributen för den matchade katalogen. I detta fall `*`rootId`*` ersätts med `attribute::RootPath` (eller `default::RootPath`, om inget anges i den här katalogen).

If `attribute::FullMatch` är inställt ignorerar servern helt katalogen, som om ingen katalog hade matchats, och fortsätter med standardkatalogattributen. I detta fall `*`rootId`*` förblir en del av banan (som föregås av `default::RootPath`).

## Egenskaper {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Flagga. Ange 0 som standardbeteende eller 1 om du vill aktivera fullständigt matchningsbeteende.

## Standard {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Ärvs från `default::FullMatch` om den inte är definierad eller om den är tom.

## Se även {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [katalog::ID](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
