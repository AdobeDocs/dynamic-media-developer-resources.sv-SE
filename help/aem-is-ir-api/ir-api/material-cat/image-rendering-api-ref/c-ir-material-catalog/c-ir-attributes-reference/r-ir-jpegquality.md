---
description: Standardkvalitet för JPEG-kodning. Anger standardkvalitetsinställningen för JPEG-kodade svarsbilder.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# JpegQuality{#jpegquality}

Standardkvalitet för JPEG-kodning. Anger standardkvalitetsinställningen för JPEG-kodade svarsbilder.

## Egenskaper {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

Heltal och flagga, avgränsade med kommatecken. Det första värdet ligger inom intervallet 1..100 och definierar kvaliteten. Det andra värdet kan vara 0 för normalt beteende, eller 1 för att inaktivera nedsampling av kromaticitet som vanligtvis används av JPEG-kodare.

## Standard {#section-60900c0fb8c54444b2361513232514db}

Ärvs från `default::JpegQuality` om det inte är definierat eller om det är tomt.

## Se även {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
