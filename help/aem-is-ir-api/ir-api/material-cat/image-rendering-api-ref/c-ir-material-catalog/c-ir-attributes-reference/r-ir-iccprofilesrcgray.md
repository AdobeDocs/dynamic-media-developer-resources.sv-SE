---
description: Standardprofil för inmatningsfärg för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalematerialbilder som inte bäddar in en färgprofil.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Standardprofil för inmatningsfärg för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalematerialbilder som inte bäddar in en färgprofil.

## Egenskaper {#section-97923d8561b845309442d57d017d91a4}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som refereras måste vara en gråskaleprofil.

## Standard {#section-02c52805ee13483dba7878aeab51f889}

Ärvs från `default::IccProfileSrcGray` om det inte är definierat eller om det är tomt. Om `attribute::IccProfileSrcGray` inte matchar en giltig profil används `attribute::IccProfileGray` i stället.

## Se även {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
