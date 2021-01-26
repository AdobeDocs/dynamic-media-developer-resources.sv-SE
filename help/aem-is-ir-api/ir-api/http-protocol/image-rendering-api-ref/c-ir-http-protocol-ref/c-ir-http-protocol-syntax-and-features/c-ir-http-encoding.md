---
description: Kommandovärden måste vara http-kodade med %xx escape-sekvenser, så att värdesträngarna inte innehåller de reserverade tecknen '=', '&' och '%'.
seo-description: Kommandovärden måste vara http-kodade med %xx escape-sekvenser, så att värdesträngarna inte innehåller de reserverade tecknen '=', '&' och '%'.
seo-title: HTTP-kodning för bildåtergivning
solution: Experience Manager
title: HTTP-kodning för bildåtergivning
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# HTTP-kodning för bildåtergivning{#image-rendering-http-encoding}

Kommandovärden måste vara http-kodade med %xx escape-sekvenser, så att värdesträngarna inte innehåller de reserverade tecknen &#39;=&#39;, &#39;&amp;&#39; och &#39;%&#39;.

Annars gäller standardreglerna för HTTP-kodning. HTTP-specifikationen kräver kodning av osäkra tecken som &#39; (blanksteg), &#39;&quot;&#39;(dubbelt citattecken), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; och &#39;>&#39;, liksom alla kontrolltecken som t.ex. `<return>` och `<tab>`.

**Varning:** Klammerparenteser {} som används som avgränsare för kapsling av begäran får inte kodas. Vissa e-postklienter kodar tyvärr klammerparenteser i inbäddad HTTP-begäran. Om detta är ett problem tillåter bildåtergivning att parenteser ( ) används i stället för klammerparenteser.

## Exempel {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Ovanstående begärandefragment måste kodas enligt följande:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Se även {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1-specifikation (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
