---
description: Tidsstämpel för ändring. Anger datum/tid då denna vinjettering senast ändrades.
seo-description: Tidsstämpel för ändring. Anger datum/tid då denna vinjettering senast ändrades.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Tidsstämpel{#timestamp}

Tidsstämpel för ändring. Anger datum/tid då denna vinjettering senast ändrades.

Om `attribute::UseLastModified` är inställt returneras det senaste `vignette::TimeStamp`- och `catalog::TimeStamp`värdet för vinjetteringen och allt material som ingår i begäran som en senast ändrad rubrik i HTTP-svaret.

>[!NOTE]
>
>Den faktiska filtiden för vinjettfilen används aldrig för detta ändamål.

`catalog::TimeStamp` används också för katalogbaserad cachevalidering (se  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Egenskaper {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Datum-/tidsvärde i Java-format. Kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*: *[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* ligger mellan 0 och 23.
* *[!DNL zzz]* är en tidszonskod på 3 eller 4 tecken, till exempel &quot;GMT&quot; eller &quot;PST&quot;. Sommartid måste anges i tidszonskoden (t.ex. PST för Pacific Standard Time och PDT för Pacific Daylight Savings Time).
* *[!DNL offset]* är en tidszonsförskjutning i timmar eller timmar:minuter, i förhållande till GMT. &quot;PDT&quot; motsvarar till exempel &quot;GMT -7&quot;.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum/tid-värdet inte är korrekt formaterat ignoreras det och ändringstiden för filen [!DNL *[!DNL catalog]*.ini] används i stället.

## Standard {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` är fältet tomt eller saknas.

## Se även {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319),  [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
