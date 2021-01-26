---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 3.7.
solution: Experience Manager
title: Nya och ändrade åtgärder
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
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

