---
title: Förfaller
description: Klientens standardtid för cache till livstid.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Förfaller{#expiration}

Klientens standardtid för cache till livstid. Anger ett standardutgångsintervall om en viss katalogpost inte innehåller en giltig `catalog::Expiration` eller `vignette::Expiration` värde. Eller om en vinjettfil eller en materialfil används direkt, i stället för som en katalogpost.

## Egenskaper {#section-8e2bade105ec4905ae5c4911f500279f}

Realnummer `0` eller större. Antal timmar till förfallodatum sedan svarsdata genererades. Ange till `0` så att svarsbilden alltid förfaller omedelbart, vilket i praktiken inaktiverar klientcachning. Ange till `-1` att markera som *upphör aldrig att gälla*.

## Standard {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Ärvs från `default::Expiration` om den inte är definierad eller om den är tom.

## Se även {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[katalog::Förfallotid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vinjett::Förfallotid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
