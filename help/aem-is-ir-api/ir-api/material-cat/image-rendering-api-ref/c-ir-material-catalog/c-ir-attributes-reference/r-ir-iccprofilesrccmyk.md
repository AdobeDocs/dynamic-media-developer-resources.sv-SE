---
description: Standardfärgprofil för CMYK-indata. Anger namnet på ICC-färgprofilen som ska användas för CMYK-materialbilder som inte bäddar in en färgprofil.
seo-description: Standardfärgprofil för CMYK-indata. Anger namnet på ICC-färgprofilen som ska användas för CMYK-materialbilder som inte bäddar in en färgprofil.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 95147b28-c87b-4337-a0eb-a962ca1e8786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

Standardfärgprofil för CMYK-indata. Anger namnet på ICC-färgprofilen som ska användas för CMYK-materialbilder som inte bäddar in en färgprofil.

## Egenskaper {#section-0cee77438d914c319ec876edb3490821}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som det hänvisas till måste vara en CMYK-profil.

## Standard {#section-11f6239e0dd14827abf4a95c1b30161c}

Ärvs från `default::IccProfileSrcCmyk` om det inte är definierat eller om det är tomt. Om `attribute::IccProfileSrcCmyk` inte matchar en giltig profil används `attribute::IccProfileCmyk` i stället.

## Se även {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
