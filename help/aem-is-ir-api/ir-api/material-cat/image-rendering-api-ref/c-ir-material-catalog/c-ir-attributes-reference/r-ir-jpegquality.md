---
description: Standardkvalitet för JPEG-kodning. Anger standardkvalitetsinställningen för JPEG-kodade svarsbilder.
seo-description: Standardkvalitet för JPEG-kodning. Anger standardkvalitetsinställningen för JPEG-kodade svarsbilder.
seo-title: JpegQuality
solution: Experience Manager
title: JpegQuality
topic: Scene7 Image Serving - Image Rendering API
uuid: 82dabdae-a1f3-484a-a520-ae765914d0f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JpegQuality{#jpegquality}

Standardkvalitet för JPEG-kodning. Anger standardkvalitetsinställningen för JPEG-kodade svarsbilder.

## Egenskaper {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

Heltal och flagga, avgränsade med kommatecken. Det första värdet ligger inom intervallet 1..100 och definierar kvaliteten. Det andra värdet kan vara 0 för normalt beteende, eller 1 för att inaktivera nedsampling av kromaticitet som vanligtvis används av JPEG-kodare.

## Standard {#section-60900c0fb8c54444b2361513232514db}

Ärvs från `default::JpegQuality` om inte definierad eller om tom.

## Se även {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
