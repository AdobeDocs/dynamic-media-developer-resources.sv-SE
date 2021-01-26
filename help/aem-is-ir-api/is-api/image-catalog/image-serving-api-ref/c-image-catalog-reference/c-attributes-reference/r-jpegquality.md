---
description: Standardattribut för JPEG-kodning. Anger standardattributen för JPEG-svarsbilder.
seo-description: Standardattribut för JPEG-kodning. Anger standardattributen för JPEG-svarsbilder.
seo-title: JpegQuality
solution: Experience Manager
title: JpegQuality
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c256c44c-2807-4a0c-b6e4-3de0a828feda
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# JpegQuality{#jpegquality}

Standardattribut för JPEG-kodning. Anger standardattributen för JPEG-svarsbilder.

## Egenskaper {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

Heltal och flagga, avgränsade med kommatecken. Det första värdet ligger inom intervallet 1..100 och definierar kvaliteten. Det andra värdet kan vara 0 för normalt beteende, eller 1 för att inaktivera nedsampling av RGB-kromaticitet som vanligtvis används av JPEG-kodare.

## Standard {#section-0b25eddd59bc434abfe38eeea9d45df3}

Ärvs från `default::JpegQuality` om det inte är definierat eller om det är tomt.

## Se även {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
