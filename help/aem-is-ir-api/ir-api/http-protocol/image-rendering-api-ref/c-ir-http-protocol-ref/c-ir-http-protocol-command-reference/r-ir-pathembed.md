---
description: Bädda in bandata. Anger om Photoshop-banor som är inbäddade i vinjetteringen ska inkluderas i svarsbilden.
seo-description: Bädda in bandata. Anger om Photoshop-banor som är inbäddade i vinjetteringen ska inkluderas i svarsbilden.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: d40ea1b5-f2d3-4f81-b96f-abb4eb7eb2b3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pathEmbed{#pathembed}

Bädda in bandata. Anger om Photoshop-banor som är inbäddade i vinjetteringen ska inkluderas i svarsbilden.

`pathEmbed=0|1`

## Egenskaper {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Begär attribut. Ignoreras om vinjetteringen inte innehåller sökvägsdata. Banans data skalas till `wid=` och/eller `hei=` om det behövs.

Ignoreras om utdatabildformatet inte stöder baninbäddning. Se beskrivningen av `fmt=` för en lista över de utdataformat som stöder baninbäddning.

## Standard {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, utan inbäddning av banor i utdatabilder.

## Se även {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
