---
description: Dessa nya eller ändrade åtgärder och datatyper som finns i betaversionen av WSDL får inte användas utanför Dynamic Media-utvecklade program.
solution: Experience Manager
title: Begränsad användning
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
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

* Ändrad `ActiveJob` att inkludera `createVideoSitemapJob` type

* Ändrad `ScheduledJob` att inkludera `createVideoSitemapJob` type

* Ändrad `ImageServingPublishJob` att inkludera `contextHandle`

* Ändrad `ImageRenderingPublishJob` att inkludera `contextHandle`

* Ändrad `MetadataField` att inkludera `initialTagField`

* Ändrad `MetadataCondition` att inkludera och valfritt `caseSensitive` parameter

* Ändrad `PropertySet` att inkludera `PermissionArray` as `permissions`

* Ändrad `UploadDirectoryJob` inkluderar valfritt `xmpKeywords`, `xmpTemplateId` och `xmpTemplateOverride` parameters

* Ändrad `VideoPublishJob` att inkludera `contextHandle`

**Ändrade åtgärder**

* Ändrad `createAssetSet` att inkludera `thumbAssetHandle`

* Ändrad `createImageSet` att inkludera `thumbAssetHandle`

* Ändrad `createMetadataField` att inkludera `initialTagValue` parameter

* Ändrad `createPropertySet` att inkludera `PermissionUpdateArray` as `permissionArray`

* Ändrad `getImageServingPublishSettings` att inkludera `contextHandle` parameter

* Ändrad `getImageRenderingPublishSettings` att inkludera `contextHandle` parameter

* Ändrad `searchAssetsByFullText` att inkludera en serie valfria parametrar:

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`

* Ändrad `searchAssetsByMetadata` att inkludera en serie valfria parametrar:

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sekvens med sju parametrar

* Ändrad `setAssetPublishState` att inkludera `HandleArray` as `contextHandleArray`

* Ändrad `setImageServingPublishSettings` att inkludera `contextHandle` parameter

* Ändrad `setImageRenderingPublishSettings` att inkludera `contextHandle`parameter

* Ändrad `submitJob` att inkludera `createVideoSitemap` jobbtyp
