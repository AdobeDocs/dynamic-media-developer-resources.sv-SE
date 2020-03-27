---
description: Bildschemadata. Inga eller fler kompletta HTML-element (<AREA>), sorterade framifrån och bakåt.
seo-description: Bildschemadata. Inga eller fler kompletta HTML-element (<AREA>), sorterade framifrån och bakåt.
seo-title: Karta
solution: Experience Manager
title: Karta
topic: Scene7 Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Karta{#map}

Bildschemadata. Inga eller fler kompletta HTML- `<AREA>` element, sorterade framifrån och bakåt.

Servern tolkar och kan ändra attributen SHAPE och COORDS. (SHAPE=CIRCLE stöds inte i den här versionen.) Alla andra attribut i `<AREA>` skickas igenom utan ändring. Koordinatvärden som anges med COORDS-attributet måste vara pixelförskjutningar från det övre vänstra hörnet i den oförändrade källbilden. (`%` koordinater stöds inte i den här versionen och kan inte behandlas korrekt.)

## Egenskaper {#section-f52d89fd399b4356ac05277e6c12f956}

Textsträngsvärde. Om det anges måste det vara ett eller flera fullständiga HTML- `<AREA>` element.

Det här fältet deltar i textsträngslokalisering. Mer information finns i Lokalisering [av](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) textsträngar i *HTTP-protokollreferensen* .

## Standard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Ingen.

## Se även {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [textsträngslokalisering](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
