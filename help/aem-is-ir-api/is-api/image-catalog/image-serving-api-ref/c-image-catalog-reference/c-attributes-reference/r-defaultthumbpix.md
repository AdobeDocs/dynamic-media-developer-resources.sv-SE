---
description: Standardstorlek för miniatyrbild. Används i stället för attributet DefaultPix för begäranden om miniatyrbilder (req=tmb).
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# DefaultThumbPix{#defaultthumbpix}

Standardstorlek för miniatyrbild. Används i stället för attribut::DefaultPix för miniatyrbegäranden (req=tmb).

Servern begränsar svarsbilder till att inte vara större än den här bredden och höjden om en miniatyrbegäran ( `req=tmb`) inte uttryckligen anger storleken utan att uttryckligen ange visningsstorleken med `wid=`, `hei=` eller `scl=`.

## Egenskaper {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Två heltal, 0 eller större, avgränsade med kommatecken. Bredd och höjd i pixlar. Antingen eller båda värdena kan anges till 0 för att behålla dem obegränsade.

Gäller inte kapslade/inbäddade begäranden.

## Standard {#section-2c4a4f14540449638822913513170ff1}

Ärvs från `default::DefaultThumbPix` om inte definierad eller om tom.

## Se även {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
