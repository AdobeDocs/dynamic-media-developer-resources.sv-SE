---
description: Gråskalans standardprofil för utdatafärg. Anger namnet på ICC-färgprofilen som ska användas för gråskalesvarsbilder när ingen utdatafärgrymd har angetts med icc= och för vissa gråskalefärgvärden som har angetts med olika bildserverkommandon, till exempel color=.
seo-description: Gråskalans standardprofil för utdatafärg. Anger namnet på ICC-färgprofilen som ska användas för gråskalesvarsbilder när ingen utdatafärgrymd har angetts med icc= och för vissa gråskalefärgvärden som har angetts med olika bildserverkommandon, till exempel color=.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a7d40114-f91f-4637-bb49-5b06b9ce846d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# IccProfileGray{#iccprofilegray}

Gråskalans standardprofil för utdatafärg. Anger namnet på ICC-färgprofilen som ska användas för gråskalesvarsbilder när ingen utdatafärgrymd har angetts med icc= och för vissa gråskalefärgvärden som har angetts med olika bildserverkommandon, till exempel color=.

## Egenskaper {#section-03f090ee2acf4537b83f78840d23ecab}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som refereras måste vara en gråskaleprofil.

## Standard {#section-95ba3ab15edc4259b657c6ebf8783d61}

Ärvs från `default::IccProfileGray` om det inte är definierat eller om det är tomt.

## Se även {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
