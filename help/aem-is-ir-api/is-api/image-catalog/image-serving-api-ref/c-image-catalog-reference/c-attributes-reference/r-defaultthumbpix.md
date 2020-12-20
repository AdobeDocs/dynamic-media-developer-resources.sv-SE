---
description: Standardstorlek för miniatyrbild. Används i stället för attributet DefaultPix för begäranden om miniatyrbilder (req=tmb).
seo-description: Standardstorlek för miniatyrbild. Används i stället för attributet DefaultPix för begäranden om miniatyrbilder (req=tmb).
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# DefaultThumbPix{#defaultthumbpix}

Standardstorlek för miniatyrbild. Används i stället för attribut::DefaultPix för miniatyrbegäranden (req=tmb).

Servern begränsar svarsbilder till att inte vara större än den här bredden och höjden om en miniatyrbegäran ( `req=tmb`) inte uttryckligen anger storleken som inte uttryckligen anger visningsstorleken med `wid=`, `hei=` eller `scl=`.

## Egenskaper {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Två heltal, 0 eller större, avgränsade med kommatecken. Bredd och höjd i pixlar. Antingen eller båda värdena kan anges till 0 för att behålla dem obegränsade.

Gäller inte kapslade/inbäddade begäranden.

## Standard {#section-2c4a4f14540449638822913513170ff1}

Ärvs från `default::DefaultThumbPix` om det inte är definierat eller om det är tomt.

## Se även {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [attribut::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
