---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 6.
seo-description: Beskriver nya och ändrade operationsmetoder för IPS API version 6.
seo-title: Nya och ändrade åtgärder
solution: Experience Manager
title: Nya och ändrade åtgärder
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---


# Åtgärder: Nytt och ändrat{#operations-new-and-modified}

Beskriver nya och ändrade operationsmetoder för IPS API version 6.

Syntax

## Nya åtgärder {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Ändrade åtgärder {#section-f4e8755527444266ae806e3f4c851ae6}

**Tillagd**

* `isHidden` och `initialTagValue` har lagts till i:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* `thumbAssetHandle` har lagts till i:

   * `createImageSet`
   * `createAssetSet`

   `companyHandle` har lagts till i:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   `contextHandle` har lagts till i:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* IncludeInactive har lagts till i:

   * `getUsers`.
   * `getUserChars`.

* `permissionArray` har lagts till i `createPropertySet`.

* `exportJob` har lagts till i `submitJob`.

**Ändrad**

* I `addUser` och `setUser` ändrades `role` till `defaultRole`.

* I `getCompanyMembers` har `userArray` ändrats till `memberArray`.

* I `getCompanyMembership` har `companyArray` ändrats till `membershipArray`.

* I `addUser`, `setCompanyMembership` och `addCompanyMembership` ändrades `membershipArray` till `companyHandleArray`.

* I `getCompanyMembership` har `companyArray` ändrats till `membershipArray`.

* I `getUserChars` är `includeInvalid` nu valfritt.

**Borttagen**

* Tog bort `renameFiles` från `renameAsset`.

* Borttagen `getXMPPanelViewDefinition`.
* Borttagen `searchAssetsByFulltext` och `searchAssetsBySimilarity`.

