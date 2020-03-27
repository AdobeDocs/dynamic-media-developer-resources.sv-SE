---
description: Felsvarsbild. Bildåtergivning returnerar vanligtvis en felstatus med ett textmeddelande när ett fel inträffar. Med attributet ErrorImage kan du konfigurera en bild som returneras vid fel.
seo-description: Felsvarsbild. Bildåtergivning returnerar vanligtvis en felstatus med ett textmeddelande när ett fel inträffar. Med attributet ErrorImage kan du konfigurera en bild som returneras vid fel.
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorImage *{#errorimage}

Felsvarsbild. Bildåtergivning returnerar vanligtvis en felstatus med ett textmeddelande när ett fel inträffar. attribute::ErrorImage tillåter konfiguration av en bild som returneras vid fel.

När ett fel inträffar försöker servern först tolka värdet för `ImageRendering::attribute::ErrorImage`som en enkel bildfilssökväg. Om filen inte kan öppnas skickas attributvärdet och felinformationen till Image Serving, som utför de processer som beskrivs i `ImageServing::attribute::ErrorImage`. Om Image Serving inte returnerar en giltig svarsbild skickas standardfelstatusen för HTTP och textmeddelandet till klienten.

Felbilder returneras med HTTP-status 200.

## Egenskaper {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Textsträng. Om det anges måste det antingen vara ett **`ImageServing::catalog::id`** värde, en relativ sökväg (till **`ImageServing::attribute::RootPath`** eller **`ImageRendering::attribute::RootPath`**) eller en absolut sökväg till en bildfil som är tillgänglig för Image Server.

## Standard {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Ärvs från `default::ErrorImage` om det inte har definierats. Om den är definierad men tom inaktiveras felbildens beteende, även om `default::ErrorImage` den är definierad, och HTTP-felstatusen returneras.

## Se även {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
