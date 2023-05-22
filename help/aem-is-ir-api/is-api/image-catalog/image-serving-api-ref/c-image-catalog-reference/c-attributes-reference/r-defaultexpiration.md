---
description: Klientcache TTL för standardbildsvar. Anger utgångsintervallet för standardbildsvar (svar som returnerar en standardbild som har angetts med defaultImage= eller attribute DefaultImage).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# DefaultExpiration{#defaultexpiration}

Klientcache TTL för standardbildsvar. Anger utgångsintervallet för standardbildsvar (svar som returnerar en standardbild som har angetts med defaultImage= eller attribute::DefaultImage).

Används bara när standardbilden inte är associerad med en katalogpost eller när standardbildkatalogposten inte innehåller någon specifik `catalog::Expiration` värde.

## Egenskaper {#section-e564512476604fd7b964f9f2903d6d33}

Reellt tal, 0 eller högre. Antal timmar till förfallodatum sedan svarsdata genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket innebär att klientcache-lagring inaktiveras för standardbildsvar. Ange till `-1` att markera som `never expire`.

## Standard {#section-131cd32c2e214391857dba5af321f8cd}

Ärvs från `default::DefaultExpiration` om den inte är definierad eller om den är tom.

TTL (Time-To-Live) är längden innan cachen förfaller. Standardvärdet för TTL är 1 timme.

## Se även {#section-d8642c22e3d947129367dd76366963d6}

[katalog::Förfallotid](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
