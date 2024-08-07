---
title: IccProfileSrcRgb
description: RGB standardfärgprofil för indata. Anger namnet på ICC-färgprofilen som ska användas för RGB-materialbilder och vinjetter som inte bäddar in en färgprofil. Även för färgvärden för RGB som anges med olika kommandon för bildåtergivning, till exempel bgc= och color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB standardfärgprofil för indata. Anger namnet på ICC-färgprofilen som ska användas för RGB-materialbilder och vinjetter som inte bäddar in en färgprofil. Även för färgvärden för RGB som anges med olika kommandon för bildåtergivning, till exempel `bgc=` och `color=`.

## Egenskaper {#section-c22966bba03e43c08e9d3fb91bfdd465}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name`-värde från ICC-profilmappningen för antingen den här bildkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som det hänvisas till måste vara en RGB-profil.

## Standard {#section-0171cd6680284bfa9844b9cc3644ca61}

Ärvs från `default::IccProfileSrcRgb` om inte definierad eller om tom. Om `attribute::IccProfileSrcRgb` inte matchar en giltig profil används `attribute::IccProfileRgb` i stället.

## Se även {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
