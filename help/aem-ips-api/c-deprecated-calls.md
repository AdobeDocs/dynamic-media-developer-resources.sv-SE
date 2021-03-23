---
title: Inaktuella anrop
description: API-anrop för bildproduktionssystem och associerade parametrar som inte längre används i Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# Inaktuella anrop{#deprecated-calls}

API-anrop till Image Production System och associerade parametrar som inte längre används.

## Inaktuella anrop {#topic-654c0466e6434fe4a95953322255b08c}

API-anrop för bildproduktionssystem och associerade parametrar som inte längre används i Dynamic Media.

* `addMediaPortalEvent` - Borttagen från åtgärder. Med det här anropet kan du lägga till en mediaportal-händelse i IPS.
* `getMediaPortalEvent` - Borttagen från åtgärder. Med det här anropet kan du hämta medieportalhändelser som matchar angivna villkor.
* `getCdnCacheInvalidationStatus` - Borttagen från åtgärder. API:t är nu föråldrat eftersom API:t `cdnCacheInvalidation` gör cache nästan omedelbart ogiltig (~5 sekunder). Därför krävs inte längre avsökning för ogiltigförklaringsstatus.

