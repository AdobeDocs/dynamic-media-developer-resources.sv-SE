---
description: Standardfärgprofil för CMYK-indata. Anger namnet på ICC-färgprofilen som ska användas för CMYK-källbilder som inte bäddar in en färgprofil och för vissa CMYK-färgvärden som anges med olika bildserverkommandon, till exempel color=.
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Standardfärgprofil för CMYK-indata. Anger namnet på ICC-färgprofilen som ska användas för CMYK-källbilder som inte bäddar in en färgprofil och för vissa CMYK-färgvärden som anges med olika bildserverkommandon, till exempel color=.

## Egenskaper {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som det hänvisas till måste vara en CMYK-profil.

## Standard {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Ärvs från `default::IccProfileSrcCmyk` om det inte är definierat eller om det är tomt. Om `attribute::IccProfileSrcCmyk` inte matchar en giltig profil används `attribute::IccProfileCmyk` i stället.

## Se även {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
