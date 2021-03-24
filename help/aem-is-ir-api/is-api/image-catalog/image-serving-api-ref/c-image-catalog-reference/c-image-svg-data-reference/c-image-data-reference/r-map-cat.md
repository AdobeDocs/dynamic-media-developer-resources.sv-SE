---
description: Bildschemadata. Inga eller fler kompletta HTML-element (<AREA>), sorterade framifrån och bakåt.
solution: Experience Manager
title: Karta
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# Karta{#map}

Bildschemadata. Inget eller flera kompletta HTML `<AREA>`-element, sorterade framifrån och bakåt.

Servern tolkar och kan ändra attributen SHAPE och COORDS. (SHAPE=CIRCLE stöds inte i den här versionen.) Alla andra attribut för `<AREA>` skickas utan ändring. Koordinatvärden som anges med COORDS-attributet måste vara pixelförskjutningar från det övre vänstra hörnet i den oförändrade källbilden. (`%` koordinater stöds inte i den här versionen och kan inte behandlas korrekt.)

## Egenskaper {#section-f52d89fd399b4356ac05277e6c12f956}

Textsträngsvärde. Om det anges måste det vara ett eller flera fullständiga HTML `<AREA>`-element.

Det här fältet deltar i textsträngslokalisering. Mer information finns i [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) i *HTTP-protokollreferens*.

## Standard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Ingen.

## Se även {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md),  [textsträngslokalisering](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
