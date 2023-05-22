---
description: Digimarc-användarinformation. Anger användarinformation för Digimarc-inbäddning.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# DigimarcId{#digimarcid}

Digimarc-användarinformation. Anger användarinformation för Digimarc-inbäddning.

## Egenskaper {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Fem eller sex kommaavgränsade heltal. Det tredje och fjärde numret används inte längre:

`creator-id, creator-pin, durability [ , chroma ]`

The `creator-id` och `creator-pin` tillhandahålls av Digimarc när tjänsten köps. De oanvända värdena ska lämnas tomma.

`durability` anger den inbäddade styrkan för Digimarc-vattenstämpeln. Den kan vara 1, 2, 3 eller 4, med 1 som indikerar svagast och 4 starkaste hållbarhet.

Ange `chroma` till 1 för att koda vattenstämpeln till bildens krominansdata eller till 0 (standard) för att koda den till luminansen. Den här inställningen ignoreras när gråskalebilder skrivs ut.

## Standard {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Ärvs från `default::DigimarcId` om den inte är definierad eller om den är tom.

## Exempel {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Ange ett test-ID för Digimarc-skapare med varaktigheten inställd på 4.

`DigimarcId= 404407,32,,,4`

## Se även {#section-75d4d2afd1df4127b31b1a82f30079d8}

[katalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
