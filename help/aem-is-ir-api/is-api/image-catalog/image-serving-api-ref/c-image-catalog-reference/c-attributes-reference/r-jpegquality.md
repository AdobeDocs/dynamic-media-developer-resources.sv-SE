---
description: Standardkodningsattribut för JPEG. Anger standardattributen för svarsbilder i JPEG.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# JpegQuality{#jpegquality}

Standardkodningsattribut för JPEG. Anger standardattributen för svarsbilder i JPEG.

## Egenskaper {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

Heltal och flagga, avgränsade med kommatecken. Det första värdet ligger inom intervallet 1..100 och definierar kvaliteten. Det andra värdet kan vara 0 för normalt beteende eller 1 för att inaktivera nedsampling av kromaticitet i RGB som normalt används av JPEG-kodare.

## Standard {#section-0b25eddd59bc434abfe38eeea9d45df3}

Ärvs från `default::JpegQuality` om den inte är definierad eller om den är tom.

## Se även {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
