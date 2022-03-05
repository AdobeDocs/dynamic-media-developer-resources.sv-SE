---
title: HTTP-kodning för bildåtergivning
description: Kommandovärden måste vara http-kodade med %xx escape-sekvenser, så att värdesträngarna inte innehåller de reserverade tecknen '=', '&' och '%'.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# HTTP-kodning för bildåtergivning{#image-rendering-http-encoding}

Kommandovärden måste vara http-kodade med %xx escape-sekvenser, så att värdesträngarna inte innehåller de reserverade tecknen &#39;=&#39;, &#39;&amp;&#39; och &#39;%&#39;.

Annars gäller standardreglerna för HTTP-kodning. HTTP-specifikationen kräver kodning av osäkra tecken som &#39; (blanksteg), &#39;&quot;&#39;(dubbelt citattecken), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; och &#39;>&#39;, liksom alla kontrolltecken, som `<return>` och `<tab>`.

**Varning:** Klammerparenteserna {} som används som avgränsare för kapsling av begäranden får inte kodas. Vissa e-postklienter kodar tyvärr klammerparenteser i inbäddad HTTP-begäran. Om det här problemet skulle vara ett problem tillåter bildåtergivning att parenteser ( ) används i stället för klammerparenteser.

## Exempel {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Ovanstående begärandefragment måste kodas enligt följande:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Se även {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1-specifikation (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
