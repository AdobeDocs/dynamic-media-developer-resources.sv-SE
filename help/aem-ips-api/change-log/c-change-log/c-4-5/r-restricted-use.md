---
description: Dessa nya eller ändrade åtgärder och datatyper som finns i betaversionen av WSDL får inte användas utanför Dynamic Media-utvecklade program.
solution: Experience Manager
title: Begränsad användning
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Begränsad användning{#restricted-use}

Dessa nya eller ändrade åtgärder och datatyper som finns i betaversionen av WSDL får inte användas utanför Dynamic Media-utvecklade program.

Dessa åtgärder och typer kan inaktiveras, ändras eller tas bort vid efterföljande systemuppdateringar.

**Nya typer**

* ResursPubliceraKontexter
* AssetPublishContextArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**Nya åtgärder**

* applyMetadataTemplate
* batchGetAssetPublishConTexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishConTexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsByLikity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Ändrade typer**

* Ändrad `ActiveJob` till att inkludera en `createVideoSitemapJob`-typ

* Ändrad `ScheduledJob` till att inkludera en `createVideoSitemapJob`-typ

* Ändrad `ImageServingPublishJob` så att den innehåller ett valfritt `contextHandle`

* Ändrad `ImageRenderingPublishJob` så att den innehåller ett valfritt `contextHandle`

* Ändrad `MetadataField` så att den innehåller ett valfritt `initialTagField`

* Ändrad `MetadataCondition` till parametern include och optional `caseSensitive`

* Ändrad `PropertySet` till att inkludera ett valfritt `PermissionArray` som `permissions`

* Ändrad `UploadDirectoryJob` till att inkludera valfria `xmpKeywords`-, `xmpTemplateId`- och `xmpTemplateOverride`-parametrar

* Ändrad `VideoPublishJob` så att den innehåller ett valfritt `contextHandle`

**Ändrade åtgärder**

* Ändrad `createAssetSet` så att den innehåller ett valfritt `thumbAssetHandle`

* Ändrad `createImageSet` så att den innehåller ett valfritt `thumbAssetHandle`

* Ändrad `createMetadataField` till att inkludera en valfri `initialTagValue`-parameter

* Ändrad `createPropertySet` till att inkludera ett valfritt `PermissionUpdateArray` som `permissionArray`

* Ändrad `getImageServingPublishSettings` till att inkludera en valfri `contextHandle`-parameter

* Ändrad `getImageRenderingPublishSettings` till att inkludera en valfri `contextHandle`-parameter

* Ändrad `searchAssetsByFullText` så att den innehåller en serie valfria parametrar:

   * `SearchFilter` som  `filters` parameter

   * `sortBy`
   * `sortDirection`

* Ändrad `searchAssetsByMetadata` så att den innehåller en serie valfria parametrar:

   * `SearchFilter` som  `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sekvens med sju parametrar

* Ändrad `setAssetPublishState` till att inkludera ett valfritt `HandleArray` som `contextHandleArray`

* Ändrad `setImageServingPublishSettings` till att inkludera en valfri `contextHandle`-parameter

* Ändrad `setImageRenderingPublishSettings` till att inkludera en valfri `contextHandle`parameter

* Ändrad `submitJob` till att inkludera en valfri `createVideoSitemap`-jobbtyp

