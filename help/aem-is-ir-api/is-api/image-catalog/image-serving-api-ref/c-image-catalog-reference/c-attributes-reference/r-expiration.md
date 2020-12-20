---
description: Klientens standardtid för cache till livstid. Anger ett standardutgångsintervall om en viss katalogpost inte innehåller ett giltigt värde för katalogförfallotid.
seo-description: Klientens standardtid för cache till livstid. Anger ett standardutgångsintervall om en viss katalogpost inte innehåller ett giltigt värde för katalogförfallotid.
seo-title: Förfaller
solution: Experience Manager
title: Förfaller
topic: Scene7 Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Förfallodatum{#expiration}

Klientens standardtid för cache till livstid. Anger ett standardintervall för förfallodatum om en viss katalogpost inte innehåller en giltig katalog::Förfallovärde.

## Egenskaper {#section-063be3b2f13a48a3a5ab8080718e9812}

Reellt tal, 0 eller högre. Antal timmar till förfallodatum sedan svarsdata genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket i praktiken inaktiverar klientcache-lagring. Ange -1 för att markera som `never expire`.

## Standard {#section-f55308b195c04083996f6717c8537634}

Ärvs från `default::Expiration` om det inte är definierat eller om det är tomt.

TTL (Time-To-Live) är längden innan cachen förfaller. Standardvärdet för TTL är 10 timmar.

## Se även {#section-b2411d99ddb14115ad475d506efd8967}

[katalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribut::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribut::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
