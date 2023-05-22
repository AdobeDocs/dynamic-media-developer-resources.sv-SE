---
description: Bildankarpunkt. Ursprungspunkt när den här bilden används som ett lager i en mall eller sammansatt bild.
solution: Experience Manager
title: Ankarpunkt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# Ankarpunkt{#anchor}

Bildankarpunkt. Ursprungspunkt när den här bilden används som ett lager i en mall eller sammansatt bild.

Definierar också standardmittpunkten för rotation.

## Egenskaper {#section-95740f14160744e7bc763094b8be40d8}

Två heltal avgränsade med kommatecken. Pixelförskjutning i förhållande till det övre vänstra hörnet i den högupplösta bilden.

Åsidosatt av `anchor=`(som i sin tur kan åsidosättas med `origin=`).

## Standard {#section-ca3a4cc837d643519eff15951f2b47a1}

Bildens mittpunkt används om fältet inte finns eller om det är tomt, och om det är en giltig bildpost (dvs. om `catalog::Path` är giltigt).

## Se även {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
