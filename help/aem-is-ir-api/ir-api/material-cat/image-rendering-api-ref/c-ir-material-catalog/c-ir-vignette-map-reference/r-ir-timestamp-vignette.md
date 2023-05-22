---
description: Tidsstämpel för ändring. Anger datum/tid då denna vinjettering senast ändrades.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Tidsstämpel för ändring. Anger datum/tid då denna vinjettering senast ändrades.

If `attribute::UseLastModified` är inställd, den senaste `vignette::TimeStamp` och `catalog::TimeStamp`värdet på vinjetteringen och allt material som ingår i begäran returneras som en senast ändrad rubrik i HTTP-svaret.

>[!NOTE]
>
>Den faktiska filtiden för vinjettfilen används aldrig för detta ändamål.

`catalog::TimeStamp` används också för katalogbaserad cachevalidering (se [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Egenskaper {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Datum-/tidsvärde i Java-format. Kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* ligger mellan 0 och 23.
* *[!DNL zzz]* är en tidszonskod på 3 eller 4 tecken, till exempel &quot;GMT&quot; eller &quot;PST&quot;. Sommartid måste anges i tidszonskoden (t.ex. PST för Pacific Standard Time och PDT för Pacific Daylight Savings Time).
* *[!DNL offset]* är en tidszonsförskjutning i timmar eller timmar:minuter, i förhållande till GMT. &quot;PDT&quot; motsvarar till exempel &quot;GMT -7&quot;.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum/tid-värdet inte är korrekt formaterat ignoreras det och ändringstiden för [!DNL *[!DNL catalog]*.ini]-filen används i stället.

## Standard {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` är fältet tomt eller saknas.

## Se även {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [katalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
