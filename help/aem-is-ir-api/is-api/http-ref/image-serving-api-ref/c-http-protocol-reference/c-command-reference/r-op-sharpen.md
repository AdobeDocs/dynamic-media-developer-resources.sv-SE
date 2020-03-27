---
description: Öka skärpan i bilder. Använder ett grundläggande skärpefilter på lagret eller på den slutliga visningsbilden, efter all skalning, om layer=comp.
seo-description: Öka skärpan i bilder. Använder ett grundläggande skärpefilter på lagret eller på den slutliga visningsbilden, efter all skalning, om layer=comp.
seo-title: op_sharpen
solution: Experience Manager
title: op_sharpen
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a00c60a-0d5c-4a99-a649-f29ebd710cf3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_sharpen{#op-sharpen}

Öka skärpan i bilder. Använder ett grundläggande skärpefilter på lagret eller på den slutliga visningsbilden, efter all skalning, om layer=comp.

`op_sharpen=0|1`

Lagermasken eller den sammansatta masken blir också skarpare.

## Egenskaper {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Lagerattribut eller vyattribut. Gäller det aktuella lagret eller den slutliga visningsbilden om `layer=comp`. Ignoreras av effektlager.

## Standard {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, utan skärpeeffekt.

## Exempel {#section-3202122df5db4e14b358ecabfb6d8b85}

Kompensera för den lilla oskärpa som orsakas av bildomsampling. Vi ökar också JPEG-kvaliteten för att undvika ytterligare JPEG-felaktigheter i kanterna med skärpa.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Se även {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
