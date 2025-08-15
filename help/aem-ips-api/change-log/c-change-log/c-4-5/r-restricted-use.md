---
description: Dessa nya eller ändrade åtgärder och datatyper som finns i betaversionen av WSDL får inte användas utanför program som utvecklats med Dynamic Media.
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

Dessa nya eller ändrade åtgärder och datatyper som finns i betaversionen av WSDL får inte användas utanför program som utvecklats med Dynamic Media.

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
* deleteCompanymetadata
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

* `ActiveJob` har ändrats så att den innehåller en `createVideoSitemapJob`-typ

* `ScheduledJob` har ändrats så att den innehåller en `createVideoSitemapJob`-typ

* `ImageServingPublishJob` har ändrats så att den innehåller ett valfritt `contextHandle`

* `ImageRenderingPublishJob` har ändrats så att den innehåller ett valfritt `contextHandle`

* `MetadataField` har ändrats så att den innehåller ett valfritt `initialTagField`

* `MetadataCondition` har ändrats till inkluderings- och valfri `caseSensitive`-parameter

* `PropertySet` har ändrats så att den innehåller ett valfritt `PermissionArray` som `permissions`

* `UploadDirectoryJob` har ändrats så att den innehåller valfria parametrar för `xmpKeywords`, `xmpTemplateId` och `xmpTemplateOverride`

* `VideoPublishJob` har ändrats så att den innehåller ett valfritt `contextHandle`

**Ändrade åtgärder**

* `createAssetSet` har ändrats så att den innehåller ett valfritt `thumbAssetHandle`

* `createImageSet` har ändrats så att den innehåller ett valfritt `thumbAssetHandle`

* `createMetadataField` har ändrats så att den innehåller en valfri `initialTagValue`-parameter

* `createPropertySet` har ändrats så att den innehåller ett valfritt `PermissionUpdateArray` som `permissionArray`

* `getImageServingPublishSettings` har ändrats så att den innehåller en valfri `contextHandle`-parameter

* `getImageRenderingPublishSettings` har ändrats så att den innehåller en valfri `contextHandle`-parameter

* `searchAssetsByFullText` har ändrats så att den innehåller en serie valfria parametrar:

   * `SearchFilter` som `filters`-parameter

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` har ändrats så att den innehåller en serie valfria parametrar:

   * `SearchFilter` som `filters`-parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sekvens av sju parametrar

* `setAssetPublishState` har ändrats så att den innehåller ett valfritt `HandleArray` som `contextHandleArray`

* `setImageServingPublishSettings` har ändrats så att den innehåller en valfri `contextHandle`-parameter

* `setImageRenderingPublishSettings` har ändrats så att den innehåller en valfri `contextHandle`parameter

* `submitJob` har ändrats så att den innehåller en valfri jobbtyp för `createVideoSitemap`
