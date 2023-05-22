---
description: Beskriver nya och ändrade typer för IPS API version 6.
solution: Experience Manager
title: Datatyper Nytt och ändrat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---

# Datatyper: Nytt och ändrat{#data-types-new-and-modified}

Beskriver nya och ändrade typer för IPS API version 6.

Syntax

## Nya typer {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## Ändrade typer {#section-56b834b1a3b843279d8715b4a4f3890b}

**Tillagd**

* Tillagd `numUrls` till `UploadUrlsJob`.

* Tillagd `fileName` till `Asset.`

* Tillagd `isHidden` till `MetadataField`.

* Tillagd `taskState` till `TaskProgress`.

* Tillagd `exportJob` till `ActiveJob` och `ScheduledJob`.

* Tillagd `optmizedPath` och `optimizedFile` till `PsdInfo`.

* Tillagd `contextHandle` till:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Följande parametrar har lagts till i `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Ändrad**

* I `User`, ändrat `role` till `defaultRole`.

* I `Folder`, ändrat `permissions` till `permissionsSetHandle`.

* I `AssetSummary`, `type` och `name` är nu valfria.
