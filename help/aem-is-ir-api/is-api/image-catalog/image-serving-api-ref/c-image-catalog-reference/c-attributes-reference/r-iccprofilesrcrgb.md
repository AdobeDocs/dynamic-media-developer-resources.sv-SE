---
description: RGB-standardfärgprofil för indata. Anger namnet på ICC-färgprofilen som ska användas för RGB-källbilder som inte bäddar in en färgprofil och för vissa RGB-färgvärden som anges med olika bildserverkommandon, till exempel color=.
seo-description: RGB-standardfärgprofil för indata. Anger namnet på ICC-färgprofilen som ska användas för RGB-källbilder som inte bäddar in en färgprofil och för vissa RGB-färgvärden som anges med olika bildserverkommandon, till exempel color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB-standardfärgprofil för indata. Anger namnet på ICC-färgprofilen som ska användas för RGB-källbilder som inte bäddar in en färgprofil och för vissa RGB-färgvärden som anges med olika bildserverkommandon, till exempel color=.

## Egenskaper {#section-3cd753196959462e9e674dab0b033d08}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name` värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en relativ filsökväg till `attribute::RootPath`. Den ICC-profil som det hänvisas till måste vara en RGB-profil.

## Standard {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Ärvs från `default::IccProfileSrcRgb` om inte definierad eller om tom. Om `attribute::IccProfileSrcRgb` inte matchar en giltig profil `attribute::IccProfileRgb` används i stället.

## Se även {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
