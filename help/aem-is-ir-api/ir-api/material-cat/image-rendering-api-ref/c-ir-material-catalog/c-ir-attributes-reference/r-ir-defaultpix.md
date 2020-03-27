---
description: Standardstorlek för återgivningsbild. Servern begränsar svarsbilder till att inte vara större än den här bredden och höjden om begäran inte uttryckligen anger visningsstorleken med wid= eller hei=.
seo-description: Standardstorlek för återgivningsbild. Servern begränsar svarsbilder till att inte vara större än den här bredden och höjden om begäran inte uttryckligen anger visningsstorleken med wid= eller hei=.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 27574811-a920-4e54-8635-5a643b8655ef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultPix{#defaultpix}

Standardstorlek för återgivningsbild. Servern begränsar svarsbilder till att inte vara större än den här bredden och höjden om begäran inte uttryckligen anger visningsstorleken med wid= eller hei=.

## Egenskaper {#section-9dc5474fc75842308796ab6440b29611}

Två heltal, 0 eller större, avgränsade med kommatecken. Bredd och höjd i pixlar. Antingen eller båda värdena kan anges till 0 för att behålla dem obegränsade.

Gäller inte kapslade/inbäddade begäranden.

## Standard {#section-1935781c561e4679aa87a5bcced8df90}

Ärvs från `default::DefaultPix` om inte definierad eller om tom.

## Se även {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribut::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
