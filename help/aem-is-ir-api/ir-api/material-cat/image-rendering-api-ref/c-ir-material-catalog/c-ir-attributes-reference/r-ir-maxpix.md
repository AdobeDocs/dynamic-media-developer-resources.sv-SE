---
description: Storleksgräns för svarsbild. Maximal bredd och höjd för svarsbilden som kan returneras till klienten.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
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
