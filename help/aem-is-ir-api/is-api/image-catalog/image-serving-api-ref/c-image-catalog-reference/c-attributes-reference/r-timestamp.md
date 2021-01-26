---
description: Standardtidsstämpel för bildändring. Anger ett standardvärde för katalogen TimeStamp.
seo-description: Standardtidsstämpel för bildändring. Anger ett standardvärde för katalogen TimeStamp.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# Tidsstämpel{#timestamp}

Standardtidsstämpel för bildändring. Tillhandahåller ett standardvärde för katalogen::TimeStamp.

Om inget anges används ändringsdatumet/-tiden för den här [!DNL *`catalog`*.ini]-filen.

## Egenskaper {#section-647066e62ce44a84b627fdd0b2f7cfec}

Datum/tid-värde. Kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* ligger mellan 0 och 23.

*`zzz`* är en tidszonskod på 3 eller 4 tecken, till exempel  `GMT` eller  `PST`. Besparingstiden för dagsljus måste anges i tidszonskoden (t.ex. `PST` för Pacific Standard Time, jämfört med `PDT` för Pacific Daylight Savings Time).

*`offset`* är en tidszonsförskjutning i timmar eller timmar:minuter, i förhållande till GMT. `PDT` motsvarar till exempel `GMT -7`.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum/tid-värdet inte är korrekt formaterat ignoreras det och ändringstiden för filen [!DNL *`catalog`*.ini] används i stället.

## Standard {#section-ac465313c97943ed97d41ea852329177}

Om den är tom eller inte definierad används filändringstiden för den här `*`katalogen`*.ini`-filen.

## Se även {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [attribut::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribut::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
