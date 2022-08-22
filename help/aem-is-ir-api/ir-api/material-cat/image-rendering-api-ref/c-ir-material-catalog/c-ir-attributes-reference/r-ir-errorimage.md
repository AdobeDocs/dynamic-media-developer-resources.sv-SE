---
title: ErrorImage
description: Felsvarsbild. Bildåtergivning returnerar vanligtvis en felstatus med ett textmeddelande när ett fel inträffar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# ErrorImage {#errorimage}

Felsvarsbild. Bildåtergivning returnerar vanligtvis en felstatus med ett textmeddelande när ett fel inträffar. The `attribute::ErrorImage` gör att en bild kan returneras om ett fel uppstår.

När ett fel inträffar försöker servern tolka värdet för `ImageRendering::attribute::ErrorImage`som en enkel bildfilssökväg. Om filen inte kan öppnas skickas attributvärdet och felinformationen till Image Serving, som utför de processer som beskrivs i `ImageServing::attribute::ErrorImage`. Om Image Serving inte returnerar en giltig svarsbild skickas standardfelstatusen för HTTP och textmeddelandet till klienten.

Felbilder returneras med HTTP-status 200.

## Egenskaper {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Textsträng. Om den anges måste den antingen vara en **`ImageServing::catalog::id`** värde, en relativ sökväg (till **`ImageServing::attribute::RootPath`** eller **`ImageRendering::attribute::RootPath`**) eller en absolut sökväg till en bildfil som är tillgänglig för Image Server.

## Standard {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Ärvs från `default::ErrorImage` om det inte är definierat. Om det är definierat men tomt inaktiveras felbildens beteende, även om `default::ErrorImage` är definierad och en HTTP-felstatus returneras.

## Se även {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [katalog::ID](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
