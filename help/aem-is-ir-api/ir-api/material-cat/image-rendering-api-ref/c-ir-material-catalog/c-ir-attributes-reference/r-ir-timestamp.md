---
description: Standardtidsstämpel för ändring. Tillhandahåller ett standardvärde för katalogen TimeStamp och vinjettering TimeStamp. Om inget anges kommer servern att använda ändringsdatumet/-tiden för den här catalog.ini-filen.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---


# Tidsstämpel{#timestamp}

Standardtidsstämpel för ändring. Tillhandahåller ett standardvärde för katalogen::TimeStamp och vinjettering::TimeStamp. Om inget anges kommer servern att använda ändringsdatumet/-tiden för den här catalog.ini-filen.

## Egenskaper {#section-910e2562b41c47b78ee6216deeabbbd5}

Datum-/tidsvärde i Java-format. Kan vara antingen heltal i millisekunder sedan midnatt, 1 januari 1970 UTC/GMT eller ett datum/tid-strängvärde med något av följande format:

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* ligger mellan 0 och 23.

*[!DNL zzz]* är en tidszonskod på 3 eller 4 tecken, till exempel &quot;GMT&quot; eller &quot;PST&quot;. Sommartid måste anges i tidszonskoden (t.ex. PST för Pacific Standard Time och PDT för Pacific Daylight Savings Time).

*[!DNL offset]* är en tidszonsförskjutning i timmar eller timmar:minuter, i förhållande till GMT. &quot;PDT&quot; motsvarar till exempel &quot;GMT -7&quot;.

Alla element i strängformaterade datum/tid-värden måste finnas. Om datum/tid-värdet inte är korrekt formaterat ignoreras det och ändringstiden för filen [!DNL *[!DNL catalog]*.ini] används i stället.

## Standard {#section-65fb29a9ea2044df8cb9fe295eb14872}

Om den är tom eller inte definieras kommer servern att använda filändringstiden för den här [!DNL *[!DNL catalog]*.ini]-filen.

## Se även {#section-764188f9b1734ad1a6270f5fecd28532}

[katalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vinjettering::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [attribut::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [attribut::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
