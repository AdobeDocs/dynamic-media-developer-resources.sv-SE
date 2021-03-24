---
description: Ett jobb som är schemalagt att köras.
solution: Experience Manager
title: Schemalagt jobb
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# Schemalagt jobb{#scheduledjob}

Ett jobb som är schemalagt att köras.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Företagshandtag. |
| `*`jobHandle`*` | `xsd:string` | Schemalagd jobbreferens. |
| `*`name`*` | `xsd:string` | Jobbnamn. |
| `*`originalName`*` | `xsd:string` | Det schemalagda jobbets ursprungliga namn. |
| `*`type`*` | `xsd:string` | Jobbtyp. |
| `*`submitUserEmail`*` | `xsd:string` | E-postadressen till den användare som schemalagt jobbet. |
| `*`locale`*` | `xsd:string` | Språkinställningen som ska användas för jobbloggsinformation och e-postlokalisering. Språk anges som `<language_code>[- <country_code>]`, där språkkoden är en gemen tvåbokstavskod enligt ISO-639, och den valfria landskoden är en gemen tvåbokstavskod enligt ISO-3166. Den nationella strängen för engelska (USA) skulle till exempel vara: `en-US`. |
| `*`description`*` | `xsd:string` | En beskrivning av jobbet som ursprungligen angavs i `submitJob`. |
| `*`execSchedule`*` | `xsd:string` | När jobbet är schemalagt att köras. |
| `*`nextFireTime`*` | `xsd:dateTime` | Datum, tid och tidszon när jobbet ska utlösas. |
| `*`timeZone`*` | `xsd:dateTime` | Tidszonen för det schemalagda jobbet. |
| `*`triggerState`*` | `xsd:int` | Val av utlösarläge för jobb. |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Jobbinformation för en bild som visar publiceringsjobb. |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Jobbinformation för ett bildåtergivningsjobb. |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | Jobbinformation för ett videopubliceringsjobb. Se [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Jobbinformation för ett serverkatalogpubliceringsjobb. |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Jobbinformation för ett uppladdningskatalogjobb. |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | Jobbinformation för ett jobb för att ladda upp URL:er. |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | Tillåt auktoriserad export av tidigare överförda filer. Se [Exportera jobb](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Anteckningar {#section-34ec157f281f412f9f0f6e861e6ed0cd}

När du anger ett jobbtypsvärde i `submitJob` returneras ett jobb baserat på den typen. Följande jobb kan returneras:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

