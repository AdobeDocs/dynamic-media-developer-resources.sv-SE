---
title: TimeStamp
description: Om "attribute::UseLastModified" är inställt returneras värdet "catalog::TimeStamp" i HTTP-svaret som ett Senast ändrat HTTP-huvud.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# TimeStamp{#timestamp}

If `attribute::UseLastModified` är inställd, `catalog::TimeStamp` värdet returneras i HTTP-svaret som en Senast ändrad HTTP-rubrik. Rubriken Senast ändrad returneras alltid för statiskt innehåll, även om `attribute::UseLastModified` har inte angetts.

För bild- och SVG-innehåll `catalog::TimeStamp` används också för katalogbaserad cachevalidering (se [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Egenskaper {#section-2298a384b5cb43929542655c5a49beb2}

Datum-/tidsvärde i Java-format. Kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* ligger mellan 0 och 23.

*`zzz`* är en tidszonskod på tre eller fyra tecken, till exempel &quot;GMT&quot; eller &quot;PST&quot;. Konto för sommartid i tidszonskoden. Till exempel PST för Pacific Standard Time jämfört med PDT för Pacific Daylight Savings Time).

*`offset`* är en tidszonsförskjutning i timmar eller `hours:minutes`, i förhållande till GMT. &quot;PDT&quot; motsvarar till exempel &quot;GMT -7&quot;.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum/tid-värdet inte är korrekt formaterat ignoreras det och ändringstiden för `*`katalog`*.ini` filen används i stället.

## Standard {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` om fältet är tomt eller inte finns.

## Se även {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
