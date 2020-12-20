---
description: RGB-standardprofil för utdatafärg. Anger namnet på ICC-färgprofilen som ska användas för RGB-svarsbilder när ingen utdatafärgrymd har angetts med icc= och för vissa RGB-färgvärden som har angetts med olika bildserverkommandon, till exempel color=.
seo-description: RGB-standardprofil för utdatafärg. Anger namnet på ICC-färgprofilen som ska användas för RGB-svarsbilder när ingen utdatafärgrymd har angetts med icc= och för vissa RGB-färgvärden som har angetts med olika bildserverkommandon, till exempel color=.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 40606151-d5fa-4ae5-b6f0-e811bfea4691
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# IccProfileRgb{#iccprofilergb}

RGB-standardprofil för utdatafärg. Anger namnet på ICC-färgprofilen som ska användas för RGB-svarsbilder när ingen utdatafärgrymd har angetts med icc= och för vissa RGB-färgvärden som har angetts med olika bildserverkommandon, till exempel color=.

## Egenskaper {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som det hänvisas till måste vara en RGB-profil.

## Standard {#section-dfe08dd7b851453ca816623a4179955b}

Ärvs från `default::IccProfileRgb` om det inte är definierat eller om det är tomt.

## Se även {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
