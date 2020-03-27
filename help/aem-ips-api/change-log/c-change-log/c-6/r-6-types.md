---
description: Beskriver nya och ändrade typer för IPS API version 6.
seo-description: Beskriver nya och ändrade typer för IPS API version 6.
seo-title: Datatyper Nytt och ändrat
solution: Experience Manager
title: Datatyper Nytt och ändrat
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

* Tillagd `numUrls` i `UploadUrlsJob`.

* Tillagd `fileName` i `Asset.`

* Tillagd `isHidden` i `MetadataField`.

* Tillagd `taskState` i `TaskProgress`.

* Tillagd `exportJob` till `ActiveJob` och `ScheduledJob`.

* Tillagd `optmizedPath` och `optimizedFile` till `PsdInfo`.

* Tillagt `contextHandle` i:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Följande parametrar har lagts till i `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Ändrad**

* In `User`, ändrad `role` till `defaultRole`.

* In `Folder`, ändrad `permissions` till `permissionsSetHandle`.

* In `AssetSummary`, `type` and `name` are now optional.

