---
description: Standardprofil för CMYK-utdata. Anger namnet på ICC-färgprofilen som ska användas för CMYK-svarsbilder när ingen utdatafärgrymd har angetts med icc= och för vissa CMYK-färgvärden som har angetts med olika bildserverkommandon, till exempel color=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# IccProfileCmyk{#iccprofilecmyk}

Standardprofil för CMYK-utdata. Anger namnet på ICC-färgprofilen som ska användas för CMYK-svarsbilder när ingen utdatafärgrymd har angetts med icc= och för vissa CMYK-färgvärden som har angetts med olika bildserverkommandon, till exempel color=.

## Egenskaper {#section-d8b6102cc1c744d482f99808ccfcaa24}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som det hänvisas till måste vara en CMYK-profil.

## Standard {#section-62442df09a724950bfbdd0640b3e6678}

Ärvs från `default::IccProfileCmyk` om inte definierad eller om tom.

## Se även {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
