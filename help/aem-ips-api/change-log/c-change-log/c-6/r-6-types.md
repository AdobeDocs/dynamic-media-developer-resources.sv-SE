---
description: Beskriver nya och ändrade typer för IPS API version 6.
solution: Experience Manager
title: Datatyper Nytt och ändrat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
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

* `numUrls` har lagts till i `UploadUrlsJob`.

* `fileName` har lagts till i `Asset.`

* `isHidden` har lagts till i `MetadataField`.

* `taskState` har lagts till i `TaskProgress`.

* `exportJob` har lagts till i `ActiveJob` och `ScheduledJob`.

* `optmizedPath` och `optimizedFile` har lagts till i `PsdInfo`.

* `contextHandle` har lagts till i:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Följande parametrar har lagts till i `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Ändrad**

* I `User` har `role` ändrats till `defaultRole`.

* I `Folder` har `permissions` ändrats till `permissionsSetHandle`.

* I `AssetSummary` är `type` och `name` nu valfria.

