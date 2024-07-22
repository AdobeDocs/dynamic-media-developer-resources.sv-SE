---
title: Inaktuella anrop
description: API-anrop för Image Production System och tillhörande parametrar som inte längre används eller stöds i  [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Inaktuella anrop{#deprecated-calls}

API-anrop till Image Production System och associerade parametrar som inte längre används.

## Inaktuella anrop {#topic-654c0466e6434fe4a95953322255b08c}

API-anrop för bildproduktionssystem och associerade parametrar som inte längre används i [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Borttagen från [Datatyper](/help/aem-ips-api/types/c-data-types/c-data-types.md). Den här parametern exkluderade den primära videon från den adaptiva videouppsättningen. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Borttagen från [Åtgärder](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Med den här parametern kan du lägga till en Media Portal-händelse i IPS.
* `getMediaPortalEvent` - Borttagen från [Åtgärder](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Med den här parametern kan du hämta medisportalhändelser som matchar angivna villkor.
* `getCdnCacheInvalidationStatus` - Borttagen från [Åtgärder](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Parametern är nu föråldrad eftersom parametern `cdnCacheInvalidation` gör cachen ogiltig nästan omedelbart (~5 sekunder). Därför krävs inte längre avsökning för ogiltigförklaringsstatus.
