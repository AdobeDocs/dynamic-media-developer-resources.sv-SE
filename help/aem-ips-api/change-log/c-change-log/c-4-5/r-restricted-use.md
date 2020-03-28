---
description: Dessa nya eller ändrade åtgärder och datatyper som finns i betaversionen av WSDL får inte användas utanför de program som utvecklats av Scene7.
seo-description: Dessa nya eller ändrade åtgärder och datatyper som finns i betaversionen av WSDL får inte användas utanför de program som utvecklats av Scene7.
seo-title: Begränsad användning
solution: Experience Manager
title: Begränsad användning
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Begränsad användning{#restricted-use}

Dessa nya eller ändrade åtgärder och datatyper som finns i betaversionen av WSDL får inte användas utanför de program som utvecklats av Scene7.

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

* Ändrad `ActiveJob` för att inkludera en `createVideoSitemapJob` typ

* Ändrad `ScheduledJob` för att inkludera en `createVideoSitemapJob` typ

* Ändrad så `ImageServingPublishJob` att den innehåller ett valfritt `contextHandle`

* Ändrad så `ImageRenderingPublishJob` att den innehåller ett valfritt `contextHandle`

* Ändrad så `MetadataField` att den innehåller ett valfritt `initialTagField`

* Ändrad `MetadataCondition` till inkluderings- och valfri `caseSensitive` parameter

* Ändrad så `PropertySet` att den innehåller ett valfritt `PermissionArray` som `permissions`

* Ändrad `UploadDirectoryJob` till att inkludera valfria `xmpKeywords`parametrar `xmpTemplateId` och `xmpTemplateOverride` -parametrar

* Ändrad så `VideoPublishJob` att den innehåller ett valfritt `contextHandle`

**Ändrade åtgärder**

* Ändrad så `createAssetSet` att den innehåller ett valfritt `thumbAssetHandle`

* Ändrad så `createImageSet` att den innehåller ett valfritt `thumbAssetHandle`

* Ändrad så `createMetadataField` att den innehåller en valfri `initialTagValue` parameter

* Ändrad så `createPropertySet` att den innehåller ett valfritt `PermissionUpdateArray` som `permissionArray`

* Ändrad så `getImageServingPublishSettings` att den innehåller en valfri `contextHandle` parameter

* Ändrad så `getImageRenderingPublishSettings` att den innehåller en valfri `contextHandle` parameter

* Ändrad så `searchAssetsByFullText` att den innehåller en serie valfria parametrar:

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`

* Ändrad så `searchAssetsByMetadata` att den innehåller en serie valfria parametrar:

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sekvens med sju parametrar

* Ändrad så `setAssetPublishState` att den innehåller ett valfritt `HandleArray` som `contextHandleArray`

* Ändrad så `setImageServingPublishSettings` att den innehåller en valfri `contextHandle` parameter

* Ändrad så `setImageRenderingPublishSettings` att den innehåller en valfri `contextHandle`parameter

* Ändrad `submitJob` till att inkludera en valfri `createVideoSitemap` jobbtyp

