---
description: Standardsvarsbild. Anger den bild- eller katalogpost som ska användas om en bildfil inte kan hittas och defaultImage= inte anges i begäran.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# DefaultImage{#defaultimage}

Standardsvarsbild. Anger den bild- eller katalogpost som ska användas om en bildfil inte kan hittas och defaultImage= inte anges i begäran.

Kan vara antingen en katalogpost (inklusive en mall) eller en relativ (till) `attribute::RootPath`) eller absolut sökväg till bildfilen. Användbart om du vill ersätta saknade bilder med standardbilder.

## Egenskaper {#section-b6d8193827c34e5f948792aba8b8daaf}

Textsträng. Om den anges måste den vara antingen en giltig `catalog::Id` värde i den här bildkatalogen eller en relativ (till `attribute::RootPath`) eller absolut sökväg till en bildfil som är tillgänglig för Image Server.

## Begränsningar {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Utländska bildkällor omfattas inte av standardbildmekanismen. ett fel returneras om en extern bildkälla inte är giltig.

## Standard {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Ärvs från `default::DefaultImage` om inte definierat. Om det är definierat men tomt inaktiveras standardbildbeteendet, även om `default::DefaultImage` är definierad.

## Se även {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [katalog::ID](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
