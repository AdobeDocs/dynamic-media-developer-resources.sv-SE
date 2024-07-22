---
description: Bildankarpunkt. Ursprungspunkt när bilden används som ett lager i en mall eller sammansatt bild.
solution: Experience Manager
title: Ankarpunkt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Ankarpunkt{#anchor}

Bildankarpunkt. Ursprungspunkt när bilden används som ett lager i en mall eller sammansatt bild.

Definierar också standardmittpunkten för rotation.

## Egenskaper {#section-95740f14160744e7bc763094b8be40d8}

Två heltal avgränsade med kommatecken. Pixelförskjutning i förhållande till det övre vänstra hörnet i den högupplösta bilden.

Åsidosätts av `anchor=` (som i sin tur kan åsidosättas av `origin=`).

## Standard {#section-ca3a4cc837d643519eff15951f2b47a1}

Bildens mittpunkt används om fältet inte finns eller om det är tomt, och om det är en giltig bildpost (d.v.s. om `catalog::Path` är giltig).

## Se även {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
