---
title: TimeStamp
description: Tidsstämpel för ändring. Anger datum/tid då denna vinjettering senast ändrades.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Tidsstämpel för ändring. Anger datum/tid då denna vinjettering senast ändrades.

Om `attribute::UseLastModified` anges returneras det senaste `vignette::TimeStamp` - och `catalog::TimeStamp`-värdet för vinjetteringen och allt material som ingår i begäran som en senast ändrad rubrik i HTTP-svaret.

>[!NOTE]
>
>Den faktiska filtiden för vinjettfilen används aldrig för detta ändamål.

`catalog::TimeStamp` används också för katalogbaserad cachevalidering. Se [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Egenskaper {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Datum-/tidsvärde i Java™-format. Det kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*&#x200B;GMT *[!DNL offset]*

* *[!DNL hh]* ligger i intervallet 0-23.
* *[!DNL zzz]* är en tidszonskod på tre eller fyra tecken, till exempel GMT eller PST. Sommartid måste anges i tidszonskoden (t.ex. PST för Pacific Standard Time och PDT för Pacific Daylight Savings Time).
* *[!DNL offset]* är en tidszonsförskjutning i timmar eller timmar :minutes i förhållande till GMT. &quot;PDT&quot; motsvarar till exempel &quot;GMT -7&quot;.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum-/tidsvärdet inte är korrekt formaterat ignoreras det och ändringstiden för filen [!DNL *[!DNL catalog]*.ini] används i stället.

## Standard {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` är fältet som är tomt eller inte finns.

## Se även {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
