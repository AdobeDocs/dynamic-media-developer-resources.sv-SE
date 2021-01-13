---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 3148cc25-3b9a-499a-b0da-1ebe9ae99f69
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# Tidsstämpel{#timestamp}

Om `attribute::UseLastModified` anges returneras `catalog::TimeStamp`-värdet i HTTP-svaret som en Senast ändrad HTTP-rubrik. Rubriken Senast ändrad returneras alltid för statiskt innehåll, även om `attribute::UseLastModified` inte har angetts.

För bild- och SVG-innehåll används `catalog::TimeStamp` även för katalogbaserad cachevalidering (se ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Egenskaper {#section-2298a384b5cb43929542655c5a49beb2}

Datum-/tidsvärde i Java-format. Kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* ligger mellan 0 och 23.

*`zzz`* är en tidszonskod på tre eller fyra tecken, till exempel &quot;GMT&quot; eller &quot;PST&quot;. Konto för sommartid i tidszonskoden. Till exempel PST för Pacific Standard Time jämfört med PDT för Pacific Daylight Savings Time).

*`offset`* är en tidszonsförskjutning i timmar eller  `hours:minutes`i förhållande till GMT. &quot;PDT&quot; motsvarar till exempel &quot;GMT -7&quot;.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum/tid-värdet inte är korrekt formaterat ignoreras det och ändringstiden för ` *`filen `*.ini` används i stället.

## Standard {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` om fältet är tomt eller inte finns.

## Se även {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
