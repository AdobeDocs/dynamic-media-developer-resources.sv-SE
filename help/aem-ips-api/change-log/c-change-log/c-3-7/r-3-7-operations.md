---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 3.7.
seo-description: Beskriver nya och ändrade operationsmetoder för IPS API version 3.7.
seo-title: Nya och ändrade åtgärder
solution: Experience Manager
title: Nya och ändrade åtgärder
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
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

