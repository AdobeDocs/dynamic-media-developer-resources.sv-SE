---
description: Bildschemadata. Ingen eller mer fullständig HTML <area> -element, sorterade från början till slut.
solution: Experience Manager
title: Karta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# Karta{#map}

Bildschemadata. Ingen eller mer fullständig HTML `<AREA>` -element, sorterade från början till slut.

Servern tolkar och kan ändra attributen SHAPE och COORDS. (SHAPE=CIRCLE stöds inte i den här versionen.) Alla andra attribut för `<AREA>` skickas utan ändring. Koordinatvärden som anges med COORDS-attributet måste vara pixelförskjutningar från det övre vänstra hörnet i den oförändrade källbilden. (`%` koordinaterna stöds inte i den här versionen och kan inte behandlas korrekt.)

## Egenskaper {#section-f52d89fd399b4356ac05277e6c12f956}

Textsträngsvärde. Om det anges måste det vara ett eller flera fullständiga HTML `<AREA>` -element.

Det här fältet deltar i textsträngslokalisering. Se [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) i *HTTP-protokollreferens* för mer information.

## Standard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Ingen.

## Se även {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
