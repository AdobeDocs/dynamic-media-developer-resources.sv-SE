---
description: Katalogmatchningsalternativ.
seo-description: Katalogmatchningsalternativ.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# FullMatch{#fullmatch}

Katalogmatchningsalternativ.

En katalogpost anges som ett `*`rootId`*/ *`imageId`*`-par i HTTP-begäranden. Vid parsning väljs en katalog om `*`rootId`*` matchar värdet `attribute::RootId` för katalogen och katalogposten identifieras genom att matcha `*`imageId`*` med värdet `catalog::Id`. Om en katalog hittas, men det inte finns någon katalogpost som matchar `*`imageId`*`, kan servern göra något av två:

Om `attribute::FullMatch` inte anges används attributen för den matchade katalogen. I det här fallet ersätts `*`rootId`*` med `attribute::RootPath` (eller `default::RootPath`, om detta inte anges i den här katalogen).

Om `attribute::FullMatch` anges ignoreras katalogen fullständigt, som om ingen katalog hade matchats, och standardkatalogattributen används. I det här fallet förblir `*`rootId`*` en del av sökvägen (som föregås av `default::RootPath`).

## Egenskaper {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Flagga. Ange 0 som standardbeteende eller 1 om du vill aktivera fullständigt matchningsbeteende.

## Standard {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Ärvs från `default::FullMatch` om det inte är definierat eller om det är tomt.

## Se även {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
