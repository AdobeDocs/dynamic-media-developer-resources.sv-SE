---
description: Klientens standardtid för cache till livstid. Innehåller ett standardintervall för förfallodatum om en viss katalogpost inte innehåller ett giltigt värde för förfallodatum eller förfallotid för katalog, eller om en vinjettfil eller en materialfil används direkt, i stället för via en katalogpost.
seo-description: Klientens standardtid för cache till livstid. Innehåller ett standardintervall för förfallodatum om en viss katalogpost inte innehåller ett giltigt värde för förfallodatum eller förfallotid för katalog, eller om en vinjettfil eller en materialfil används direkt, i stället för via en katalogpost.
seo-title: Förfaller
solution: Experience Manager
title: Förfaller
uuid: 2b56f9ec-2b25-4e6a-aead-6dad3d2df975
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Förfallodatum{#expiration}

Klientens standardtid för cache till livstid. Innehåller ett standardintervall för förfallodatum om en viss katalogpost inte innehåller en giltig katalog::Förfallotid eller vinjett::Förfallodatum eller om en vinjettfil eller materialfil används direkt, i stället för via en katalogpost.

## Egenskaper {#section-8e2bade105ec4905ae5c4911f500279f}

Reellt tal, 0 eller högre. Antal timmar till förfallodatum sedan svarsdata genererades. Ange 0 om du alltid vill att svarsbilden ska upphöra att gälla omedelbart, vilket i praktiken inaktiverar klientcache-lagring. Ange -1 för att markera som *upphör aldrig*.

## Standard {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Ärvs från standard::Förfallodatum om inte definierat eller om tomt.

## Se även {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[katalog::Förfallotid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [vinjett::Förfallotid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
