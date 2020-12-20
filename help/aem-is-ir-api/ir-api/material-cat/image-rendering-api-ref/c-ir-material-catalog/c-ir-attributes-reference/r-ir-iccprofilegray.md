---
description: Standardfärgrymd för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalesvarsbilder när ingen utdatafärgrymd har angetts med icc=.
seo-description: Standardfärgrymd för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalesvarsbilder när ingen utdatafärgrymd har angetts med icc=.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: 064be242-d964-4fb8-99ea-78bb5599e70f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# IccProfileGray{#iccprofilegray}

Standardfärgrymd för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalesvarsbilder när ingen utdatafärgrymd har angetts med icc=.

## Egenskaper {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här materialkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som refereras måste vara en gråskaleprofil.

## Standard {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Ärvs från `default::IccProfileGray` om det inte är definierat eller om det är tomt.

## Se även {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
