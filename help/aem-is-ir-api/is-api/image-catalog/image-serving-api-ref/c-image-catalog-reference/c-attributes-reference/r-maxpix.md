---
description: Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# MaxPix{#maxpix}

Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.

Servern returnerar ett fel om en begäran skulle orsaka en svarsbild vars bredd eller höjd är större än `attribute::MaxPix`.

## Egenskaper {#section-b175425b9e9f48e0b1a71640f6a9e936}

Två heltal, större än 0, avgränsade med kommatecken. Bredd och höjd i pixlar. Kan även anges till `0,0` för att tillåta en svarsbildstorlek utan begränsningar.

## Standard {#section-1003537434da432fb2af100ecdbf9d72}

Ärvs från `default::MaxPix` om det inte är definierat eller om det är tomt.

## Se även {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
