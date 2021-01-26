---
title: Inaktuella anrop
description: API-anrop för bildproduktionssystem och associerade parametrar som inte längre används i Dynamic Media.
solution: Experience Manager
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Inaktuella anrop{#deprecated-calls}

API-anrop för bildproduktionssystem och associerade parametrar som inte längre används.

## Inaktuella anrop {#topic-654c0466e6434fe4a95953322255b08c}

API-anrop för bildproduktionssystem och associerade parametrar som inte längre används i Dynamic Media.

* `addMediaPortalEvent` - Borttagen från åtgärder. Med det här anropet kan du lägga till en mediaportal-händelse i IPS.
* `getMediaPortalEvent` - Borttagen från åtgärder. Med det här anropet kan du hämta medieportalhändelser som matchar angivna villkor.
* `getCdnCacheInvalidationStatus` - Borttagen från åtgärder. API:t är nu föråldrat eftersom API:t `cdnCacheInvalidation` gör cache nästan omedelbart ogiltig (~5 sekunder). Därför krävs inte längre avsökning för ogiltigförklaringsstatus.

