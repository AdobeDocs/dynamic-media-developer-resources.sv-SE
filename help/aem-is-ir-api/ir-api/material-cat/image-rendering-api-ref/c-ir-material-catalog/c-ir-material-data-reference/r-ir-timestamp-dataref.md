---
title: TimeStamp
description: Tidsstämpel för filändring. Anger datum/tid då bilden och/eller datafilerna som bifogats till den här katalogposten senast ändrades.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Tidsstämpel för filändring. Anger datum/tid då bilden och/eller datafilerna som bifogats till den här katalogposten senast ändrades.

Om `attribute::UseLastModified` anges returneras det senaste av `catalog::TimeStamp` - och `vignette::TimeStamp`-värdena för allt material och den vinjett som ingår i begäran som en senast ändrad rubrik i HTTP-svaret.

>[!NOTE]
>
>De faktiska filtiderna för den bild eller de datafiler som är kopplade till den här katalogposten används aldrig för detta ändamål.

`catalog::TimeStamp` används också för katalogbaserad cachevalidering (se [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Egenskaper {#section-42f09e375e72492b87a3a486da7df808}

Datum-/tidsvärde i Java™-format. Det kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* ligger i intervallet 0-23.
* *[!DNL zzz]* är en tidszonskod på tre eller fyra tecken, till exempel GMT eller PST. Sommartid för sommartid måste räknas med i tidszonskoden. Till exempel PST för Pacific Standard Time och PDT för Pacific Daylight Savings Time.
* *[!DNL offset]* är en tidszonsförskjutning i timmar eller timmar:minuter i förhållande till GMT. &quot;PDT&quot; motsvarar till exempel &quot;GMT -7&quot;.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum-/tidsvärdet inte är korrekt formaterat ignoreras det och ändringstiden för filen *catalog*.ini används i stället.

## Standard {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` är fältet som är tomt eller inte finns.

## Se även {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
