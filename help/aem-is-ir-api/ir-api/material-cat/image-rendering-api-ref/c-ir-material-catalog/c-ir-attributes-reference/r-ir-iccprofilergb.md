---
title: IccProfileRgb
description: RGB standardprofil för utdatafärg. Anger namnet på ICC-färgprofilen som ska användas för svarsbilder i RGB när ingen utdatafärgrymd har angetts med icc=. Dessutom för vissa RGB-färgvärden som anges med olika kommandon för bildåtergivning, till exempel bgc= och color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# IccProfileRgb{#iccprofilergb}

RGB standardprofil för utdatafärg. Anger namnet på ICC-färgprofilen som ska användas för svarsbilder i RGB när ingen utdatafärgrymd har angetts med `icc=`. Dessutom för vissa RGB-färgvärden som anges med olika kommandon för bildåtergivning, t.ex. `bgc=` och `color=`.

## Egenskaper {#section-b4a1bd92e99047479a5036413525a6d9}

Textsträng. Om det anges måste det vara ett giltigt `icc::Name` värde från ICC-profilmappningen för antingen den här materialkatalogen eller standardkatalogen, eller en filsökväg som är relativ till `attribute::RootPath`. Den ICC-profil som det hänvisas till måste vara en RGB-profil.

## Standard {#section-5809772f8e96438ab7626d323c66a4ba}

Ärvs från `default::IccProfileRgb` om den inte är definierad eller om den är tom.

## Se även {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
