---
description: Bildankarpunkt. Ursprungspunkt när den här bilden används som ett lager i en mall eller sammansatt bild.
solution: Experience Manager
title: Ankarpunkt
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# Ankarpunkt{#anchor}

Bildankarpunkt. Ursprungspunkt när den här bilden används som ett lager i en mall eller sammansatt bild.

Definierar också standardmittpunkten för rotation.

## Egenskaper {#section-95740f14160744e7bc763094b8be40d8}

Två heltal avgränsade med kommatecken. Pixelförskjutning i förhållande till det övre vänstra hörnet i den högupplösta bilden.

Åsidosätts med `anchor=` (som i sin tur kan åsidosättas med `origin=`).

## Standard {#section-ca3a4cc837d643519eff15951f2b47a1}

Bildens mittpunkt används om det här fältet inte finns eller om det är tomt och om det är en giltig bildpost (d.v.s. om `catalog::Path` är giltig).

## Se även {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
