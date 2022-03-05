---
title: Scenkoordinater
description: Scenens koordinatmodell används för att ange storlekar och avstånd på texturerbara objektytor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Scenkoordinater{#scene-coordinates}

Scenens koordinatmodell används för att ange storlekar och avstånd på texturerbara objektytor.

Eftersom de flesta vinjetteringar är verkliga scener som avbildar fysiska objekt, skapas de flesta vinjetter med tum som enheter för scenens koordinatmodell. Andra enheter, som mm eller cm, kan också användas. Bildåtergivning stöder inte enhetskonvertering.

Följande kommandon tar emot värden i scenens koordinatmodell:

* [grout=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [size=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
