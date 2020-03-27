---
description: Rot-URL för relativa bild-URL:er. Anger rot-URL:en för relativa bild-URL:er.
seo-description: Rot-URL för relativa bild-URL:er. Anger rot-URL:en för relativa bild-URL:er.
seo-title: RootUrl
solution: Experience Manager
title: RootUrl
topic: Scene7 Image Serving - Image Rendering API
uuid: 173ce99a-f87e-4700-a28a-1a87b8c55b85
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RootUrl{#rooturl}

Rot-URL för relativa bild-URL:er. Anger rot-URL:en för relativa bild-URL:er.

`attribute::RootUrl` används i stället för `attribute::RootPath` när ett `src=` eller `mask=` värde omges av {curly braces} eller (parenteser).

## Egenskaper {#section-fe02269b4b724319a5d1f2cfcae31cba}

Textsträngsvärde. Absolut URL-rotsökväg, inklusive den inledande protokollidentifieraren. Följande protokoll stöds: HTTP, HTTPS och FTP.

## Standard {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Ärvs från `default::RootUrl` om inte definierat. Om den är definierad men tom stöds inte relativa URL:er av den här bildkatalogen.

## Se även {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribut:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [linjeset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
