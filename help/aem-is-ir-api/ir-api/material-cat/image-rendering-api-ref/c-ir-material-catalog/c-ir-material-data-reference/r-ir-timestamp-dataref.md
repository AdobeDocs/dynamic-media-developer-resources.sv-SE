---
description: Tidsstämpel för filändring. Anger datum/tid då bilden och/eller datafilerna som bifogats till den här katalogposten senast ändrades.
seo-description: Tidsstämpel för filändring. Anger datum/tid då bilden och/eller datafilerna som bifogats till den här katalogposten senast ändrades.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

Tidsstämpel för filändring. Anger datum/tid då bilden och/eller datafilerna som bifogats till den här katalogposten senast ändrades.

Om `attribute::UseLastModified` är inställt returneras det senaste av `catalog::TimeStamp` - och `vignette::TimeStamp` -värdena för allt material och den vinjett som ingår i begäran som en senast ändrad rubrik i HTTP-svaret.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>De faktiska filtiderna för den bild eller de datafiler som är kopplade till den här katalogposten används aldrig för detta ändamål.

`catalog::TimeStamp` används också för katalogbaserad cachevalidering (se ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Egenskaper {#section-42f09e375e72492b87a3a486da7df808}

Datum-/tidsvärde i Java-format. Kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* ligger mellan 0 och 23.
* *[!DNL zzz]* är en tidszonskod på 3 eller 4 tecken, till exempel &quot;GMT&quot; eller &quot;PST&quot;. Sommartid måste anges i tidszonskoden (t.ex. PST för Pacific Standard Time och PDT för Pacific Daylight Savings Time).
* *[!DNL offset]* är en tidszonsförskjutning i timmar eller timmar:minuter, i förhållande till GMT. &quot;PDT&quot; motsvarar till exempel &quot;GMT -7&quot;.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum/tid-värdet inte är korrekt formaterat ignoreras det och ändringstiden för *filen catalog*.ini används i stället.

## Standard {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` är fältet tomt eller saknas.

## Se även {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
