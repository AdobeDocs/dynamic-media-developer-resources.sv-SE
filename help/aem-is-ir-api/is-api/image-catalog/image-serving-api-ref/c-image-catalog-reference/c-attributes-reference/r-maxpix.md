---
description: Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.
seo-description: Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MaxPix{#maxpix}

Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.

Servern returnerar ett fel om en begäran skulle orsaka en svarsbild vars bredd eller höjd är större än `attribute::MaxPix`.

## Egenskaper {#section-b175425b9e9f48e0b1a71640f6a9e936}

Två heltal, större än 0, avgränsade med kommatecken. Bredd och höjd i pixlar. Kan även ställas in så att `0,0` svarsbildens storlek tillåts utan begränsningar.

## Standard {#section-1003537434da432fb2af100ecdbf9d72}

Ärvs från `default::MaxPix` om inte definierad eller om tom.

## Se även {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
