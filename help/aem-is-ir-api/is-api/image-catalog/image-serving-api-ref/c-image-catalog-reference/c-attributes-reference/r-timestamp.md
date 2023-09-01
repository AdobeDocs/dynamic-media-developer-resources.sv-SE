---
title: TimeStamp
description: Standardtidsstämpel för bildändring. Det innehåller ett standardvärde för katalogen TimeStamp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Standardtidsstämpel för bildändring. Tillhandahåller ett standardvärde för katalogen::TimeStamp.

Om inget anges används ändringsdatumet/tiden för den här [!DNL *`catalog`*.ini] -fil.

## Egenskaper {#section-647066e62ce44a84b627fdd0b2f7cfec}

Datum/tid-värde. Det kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

Datum/tid-värdet *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

Datum/tid-värdet *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

Tidsvärdet *`hh`* ligger i intervallet 0-23.

Tidsvärdet *`zzz`* är en tidszonskod på tre eller fyra tecken som `GMT` eller `PST`. Besparingstiden för dagsljus måste räknas med i tidszonskoden (till exempel `PST` för Stillahavsområdet, normaltid `PDT` för Pacific, sommartid).

Tidsvärdet *`offset`* är en tidszonsförskjutning i timmar eller timmar:minuter, i förhållande till GMT. Till exempel: `PDT` motsvarar `GMT -7`.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum/tid-värdet inte är korrekt formaterat ignoreras det och ändringstiden för [!DNL *`catalog`*.ini] filen används i stället.

## Standard {#section-ac465313c97943ed97d41ea852329177}

Om den är tom eller inte definierad används filändringstiden för den här `*`katalog`*.ini` -fil.

## Se även {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
