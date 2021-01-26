---
description: Standardprofil för inmatningsfärg för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalekällbilder som inte bäddar in en färgprofil och för vissa gråskalefärgvärden som anges med olika bildserverkommandon, till exempel color=.
seo-description: Standardprofil för inmatningsfärg för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalekällbilder som inte bäddar in en färgprofil och för vissa gråskalefärgvärden som anges med olika bildserverkommandon, till exempel color=.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Standardprofil för inmatningsfärg för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalekällbilder som inte bäddar in en färgprofil och för vissa gråskalefärgvärden som anges med olika bildserverkommandon, till exempel color=.

## Egenskaper {#section-8cbb316df6eb463aaca7b308d3568086}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som refereras måste vara en gråskaleprofil.

## Standard {#section-bcc7250715884412bd0780f60d1cce7b}

Ärvs från `default::IccProfileSrcGray` om det inte är definierat eller om det är tomt. Om `attribute::IccProfileSrcGray` inte matchar en giltig profil används `attribute::IccProfileGray` i stället.

## Se även {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
