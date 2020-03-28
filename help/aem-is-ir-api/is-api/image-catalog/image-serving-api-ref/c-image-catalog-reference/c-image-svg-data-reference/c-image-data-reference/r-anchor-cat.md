---
description: Bildankarpunkt. Ursprungspunkt när den här bilden används som ett lager i en mall eller sammansatt bild.
seo-description: Bildankarpunkt. Ursprungspunkt när den här bilden används som ett lager i en mall eller sammansatt bild.
seo-title: Ankarpunkt
solution: Experience Manager
title: Ankarpunkt
topic: Scene7 Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Ankarpunkt{#anchor}

Bildankarpunkt. Ursprungspunkt när den här bilden används som ett lager i en mall eller sammansatt bild.

Definierar också standardmittpunkten för rotation.

## Egenskaper {#section-95740f14160744e7bc763094b8be40d8}

Två heltal avgränsade med kommatecken. Pixelförskjutning i förhållande till det övre vänstra hörnet i den högupplösta bilden.

Åsidosätts av `anchor=`(som i sin tur kan åsidosättas av `origin=`).

## Standard {#section-ca3a4cc837d643519eff15951f2b47a1}

Bildens mittpunkt används om det här fältet inte finns eller om det är tomt och om det är en giltig bildpost (dvs. om `catalog::Path` det är giltigt).

## Se även {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
