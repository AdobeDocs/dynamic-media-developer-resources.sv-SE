---
description: API-anrop för bildproduktionssystem och associerade parametrar som inte längre används.
seo-description: API-anrop för bildproduktionssystem och associerade parametrar som inte längre används.
seo-title: Inaktuella anrop
solution: Experience Manager
title: Inaktuella anrop
topic: Scene7 Image Production System API
uuid: 03925728-f011-45f0-84a6-808dff0fd529
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Inaktuella anrop{#deprecated-calls}

API-anrop för bildproduktionssystem och associerade parametrar som inte längre används.

## Inaktuella anrop {#topic-654c0466e6434fe4a95953322255b08c}

API-anrop för bildproduktionssystem och associerade parametrar som inte längre används.

* `addMediaPortalEvent` - Borttagen från åtgärder. Med det här anropet kan du lägga till en mediaportal-händelse i IPS.
* `getMediaPortalEvent` - Borttagen från åtgärder. Med det här anropet kan du hämta medieportalhändelser som matchar angivna villkor.
* `getCdnCacheInvalidationStatus` - Borttagen från åtgärder. API:t är nu föråldrat eftersom API:t `cdnCacheInvalidation` gör cache nästan omedelbart ogiltig (~5 sekunder). Därför krävs inte längre avsökning för ogiltigförklaringsstatus.

