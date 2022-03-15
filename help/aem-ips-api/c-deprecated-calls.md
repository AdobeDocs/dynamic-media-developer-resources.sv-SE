---
title: Inaktuella anrop
description: API-anrop till Image Production System och tillhörande parametrar som inte längre används eller stöds i Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 25d9de1d9ba727e72c031ab22c47bd2be5c11050
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Inaktuella anrop{#deprecated-calls}

API-anrop till Image Production System och associerade parametrar som inte längre används.

## Inaktuella anrop {#topic-654c0466e6434fe4a95953322255b08c}

API-anrop för bildproduktionssystem och associerade parametrar som inte längre används i Dynamic Media.

* `ExcludeMasterVideoFromAVS` - Borttagen från [Datatyper](/help/aem-ips-api/types/c-data-types/c-data-types.md). Den här parametern exkluderade den primära videon från den adaptiva videouppsättningen.
   >[!IMPORTANT]
   >
   >Adobe upphör med stödet för denna parameter den 1 september 2022. Se även [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md).

* `addMediaPortalEvent` - Borttagen från [Operationer](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Med den här parametern kan du lägga till en Media Portal-händelse i IPS.
* `getMediaPortalEvent` - Borttagen från [Operationer](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Med den här parametern kan du hämta medisportalhändelser som matchar angivna villkor.
* `getCdnCacheInvalidationStatus` - Borttagen från [Operationer](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Parametern är nu föråldrad eftersom `cdnCacheInvalidation` -parametern gör cacheminnet nästan omedelbart ogiltigt (~5 sekunder). Därför krävs inte längre avsökning för ogiltigförklaringsstatus.
