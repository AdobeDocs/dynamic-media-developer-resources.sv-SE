---
description: Standardprofil för inmatningsfärg för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalematerialbilder som inte bäddar in en färgprofil.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Standardprofil för inmatningsfärg för gråskala. Anger namnet på ICC-färgprofilen som ska användas för gråskalematerialbilder som inte bäddar in en färgprofil.

## Egenskaper {#section-97923d8561b845309442d57d017d91a4}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name` värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som refereras måste vara en gråskaleprofil.

## Standard {#section-02c52805ee13483dba7878aeab51f889}

Ärvs från `default::IccProfileSrcGray` om den inte är definierad eller om den är tom. If `attribute::IccProfileSrcGray` matchar inte en giltig profil, `attribute::IccProfileGray` används i stället.

## Se även {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
