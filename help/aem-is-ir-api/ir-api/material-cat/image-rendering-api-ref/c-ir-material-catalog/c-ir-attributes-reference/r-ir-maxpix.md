---
description: Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.
seo-description: Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# MaxPix{#maxpix}

Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.

Servern returnerar ett fel om en begäran skulle orsaka en svarsbild vars bredd och/eller höjd är större än `attribute::MaxSize`.

## Egenskaper {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Två heltal, större än 0, avgränsade med kommatecken. Bredd och höjd i pixlar. Kan även anges till 0,0 för att tillåta en svarsbildstorlek utan begränsningar.

## Standard {#section-45b38dc661854d11b97df5709f4f3434}

Ärvs från standard::MaxPix om inte definierad eller om tom.

## Se även {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
