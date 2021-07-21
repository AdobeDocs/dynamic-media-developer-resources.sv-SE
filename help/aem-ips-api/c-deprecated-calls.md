---
title: Inaktuella anrop
description: API-anrop för bildproduktionssystem och associerade parametrar som inte längre används i Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Inaktuella anrop{#deprecated-calls}

API-anrop till Image Production System och associerade parametrar som inte längre används.

## Inaktuella anrop {#topic-654c0466e6434fe4a95953322255b08c}

API-anrop för bildproduktionssystem och associerade parametrar som inte längre används i Dynamic Media.

* `addMediaPortalEvent` - Borttagen från åtgärder. Med det här anropet kan du lägga till en mediaportal-händelse i IPS.
* `getMediaPortalEvent` - Borttagen från åtgärder. Med det här anropet kan du hämta medieportalhändelser som matchar angivna villkor.
* `getCdnCacheInvalidationStatus` - Borttagen från åtgärder. API:t är nu föråldrat eftersom API:t `cdnCacheInvalidation` gör cache nästan omedelbart ogiltig (~5 sekunder). Därför krävs inte längre avsökning för ogiltigförklaringsstatus.
