---
description: Klientcache TTL för standardbildsvar. Anger utgångsintervallet för standardbildsvar (svar som returnerar en standardbild som har angetts med defaultImage= eller attribute DefaultImage).
seo-description: Klientcache TTL för standardbildsvar. Anger utgångsintervallet för standardbildsvar (svar som returnerar en standardbild som har angetts med defaultImage= eller attribute DefaultImage).
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# DefaultExpiration{#defaultexpiration}

Klientcache TTL för standardbildsvar. Anger utgångsintervallet för standardbildsvar (svar som returnerar en standardbild som har angetts med defaultImage= eller attribute::DefaultImage).

Används bara när standardbilden inte är associerad med en katalogpost eller när standardbildkatalogposten inte har ett specifikt `catalog::Expiration`-värde.

## Egenskaper {#section-e564512476604fd7b964f9f2903d6d33}

Reellt tal, 0 eller högre. Antal timmar till förfallodatum sedan svarsdata genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket innebär att klientcache-lagring inaktiveras för standardbildsvar. Ange `-1` som `never expire`.

## Standard {#section-131cd32c2e214391857dba5af321f8cd}

Ärvs från `default::DefaultExpiration` om det inte är definierat eller om det är tomt.

TTL (Time-To-Live) är längden innan cachen förfaller. Standardvärdet för TTL är 1 timme.

## Se även {#section-d8642c22e3d947129367dd76366963d6}

[katalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribut::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
