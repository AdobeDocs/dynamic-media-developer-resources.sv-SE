---
description: Standardsvarsbild. Anger den bild- eller katalogpost som ska användas om en bildfil inte kan hittas och defaultImage= inte anges i begäran.
seo-description: Standardsvarsbild. Anger den bild- eller katalogpost som ska användas om en bildfil inte kan hittas och defaultImage= inte anges i begäran.
seo-title: DefaultImage
solution: Experience Manager
title: DefaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8f50af-15bb-4333-b227-3eba38653a7d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# DefaultImage{#defaultimage}

Standardsvarsbild. Anger den bild- eller katalogpost som ska användas om en bildfil inte kan hittas och defaultImage= inte anges i begäran.

Kan vara antingen en katalogpost (inklusive en mall), en relativ (till `attribute::RootPath`) eller en absolut sökväg till bildfilen. Användbart om du vill ersätta saknade bilder med standardbilder.

## Egenskaper {#section-b6d8193827c34e5f948792aba8b8daaf}

Textsträng. Om det anges måste det antingen vara ett giltigt `catalog::Id` värde i den här bildkatalogen eller en relativ (till `attribute::RootPath`) eller absolut sökväg till en bildfil som är tillgänglig för bildservern.

## Begränsningar {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Utländska bildkällor omfattas inte av standardbildmekanismen. ett fel returneras om en extern bildkälla inte är giltig.

## Standard {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Ärvs från `default::DefaultImage` om inte definierat. Om det är definierat men tomt inaktiveras standardbildbeteendet, även om det `default::DefaultImage` är definierat.

## Se även {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
