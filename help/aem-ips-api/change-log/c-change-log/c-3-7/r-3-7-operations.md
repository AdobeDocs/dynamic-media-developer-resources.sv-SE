---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 3.7.
solution: Experience Manager
title: Nya och ändrade åtgärder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
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

* Borttagen `name` parameter.
* Tillagd `excludeFieldArray`.

**getFolders**

* Tillagd `excludeFieldArray`.

**getFolderTree**

* Tillagd `excludeFieldArray` och `getUniqueMetadataValues`.
* Gjord `fieldHandle` en obligatorisk parameter.
