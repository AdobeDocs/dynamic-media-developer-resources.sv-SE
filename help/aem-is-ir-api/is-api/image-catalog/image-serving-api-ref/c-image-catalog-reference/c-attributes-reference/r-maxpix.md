---
description: Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
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
