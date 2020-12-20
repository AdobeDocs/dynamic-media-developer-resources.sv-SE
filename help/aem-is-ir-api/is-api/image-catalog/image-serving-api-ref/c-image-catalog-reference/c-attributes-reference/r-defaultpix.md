---
description: Standardvisningsstorlek.
seo-description: Standardvisningsstorlek.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# DefaultPix{#defaultpix}

Standardvisningsstorlek.

Servern begränsar svarsbilderna till att inte vara större än den här bredden och höjden om begäran inte uttryckligen anger visningsstorleken med `wid=`, `hei=` eller `scl=`.

## Egenskaper {#section-c3e658cf82c540d986b118f74f0fe1b2}

Två heltal, 0 eller större, avgränsade med kommatecken. Bredd och höjd i pixlar. Antingen eller båda värdena kan anges till 0 för att behålla dem obegränsade.

Gäller inte kapslade/inbäddade begäranden.

## Standard {#section-b7338b2bf5114fff83b0714a57b20639}

Ärvs från `default::DefaultPix` om det inte är definierat eller om det är tomt.

## Se även {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [katalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
