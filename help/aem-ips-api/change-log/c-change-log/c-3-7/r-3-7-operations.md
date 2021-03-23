---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 3.7.
solution: Experience Manager
title: Nya och ändrade åtgärder
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---


# Åtgärder: Nytt och ändrat{#operations-new-and-modified}

Beskriver nya och ändrade operationsmetoder för IPS API version 3.7.

Syntax

## Nya åtgärder {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## Ändrade åtgärder {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Ta bort parametern `name`.
* `excludeFieldArray` har lagts till.

**getFolders**

* `excludeFieldArray` har lagts till.

**getFolderTree**

* `excludeFieldArray` och `getUniqueMetadataValues` har lagts till.
* Gör `fieldHandle` till en obligatorisk parameter.

