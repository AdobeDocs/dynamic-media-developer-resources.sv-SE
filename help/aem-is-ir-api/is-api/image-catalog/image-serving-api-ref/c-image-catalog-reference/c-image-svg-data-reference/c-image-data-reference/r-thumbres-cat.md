---
description: Upplösning för miniatyrbilder. Anger objektupplösningen för miniatyrbilden.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# ThumbRes{#thumbres}

Upplösning för miniatyrbilder. Anger objektupplösningen för miniatyrbilden.

Används endast om `catalog::ThumbType=3`.

## Egenskaper {#section-ee5cae086a3d4875805fa8a08756a586}

Reellt talvärde större än 0. Måste ha samma enheter som `catalog::Resolution`.

## Standard {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` används om fältet inte finns, om värdet är 0 eller om fältet är tomt.

## Se även {#section-eb716bf647614db083020fe8ce453751}

[katalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , [katalog::Upplösning](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [attribute::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Skalning av miniatyrbilder](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
