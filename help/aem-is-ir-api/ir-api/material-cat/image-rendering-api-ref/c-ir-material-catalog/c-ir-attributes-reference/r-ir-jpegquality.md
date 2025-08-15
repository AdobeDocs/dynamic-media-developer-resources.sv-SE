---
title: JpegQuality
description: Standardkvalitet för JPEG-kodning. Anger standardkvalitetsinställningen för JPEG-kodade svarsbilder.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# JpegQuality{#jpegquality}

Standardkvalitet för JPEG-kodning. Anger standardkvalitetsinställningen för JPEG-kodade svarsbilder.

## Egenskaper {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

Heltal och flagga, avgränsade med komma. Det första värdet ligger inom intervallet 1..100 och definierar kvaliteten. Det andra värdet kan vara `0` för normalt beteende eller `1` för att inaktivera nedsampling av kromaticitet som används av JPEG-kodare.

## Standard {#section-60900c0fb8c54444b2361513232514db}

Ärvs från `default::JpegQuality` om inte definierad eller om tom.

## Se även {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
