---
description: RGB-standardfärgprofil för indata. Anger namnet på ICC-färgprofilen som ska användas för RGB-källbilder som inte bäddar in en färgprofil och för vissa RGB-färgvärden som anges med olika bildserverkommandon, till exempel color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB-standardfärgprofil för indata. Anger namnet på ICC-färgprofilen som ska användas för RGB-källbilder som inte bäddar in en färgprofil och för vissa RGB-färgvärden som anges med olika bildserverkommandon, till exempel color=.

## Egenskaper {#section-3cd753196959462e9e674dab0b033d08}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som det hänvisas till måste vara en RGB-profil.

## Standard {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Ärvs från `default::IccProfileSrcRgb` om det inte är definierat eller om det är tomt. Om `attribute::IccProfileSrcRgb` inte matchar en giltig profil används `attribute::IccProfileRgb` i stället.

## Se även {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
