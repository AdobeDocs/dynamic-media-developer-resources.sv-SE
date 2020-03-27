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

* Tillagt `isHidden` och `initialTagValue` till:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Tillagt `thumbAssetHandle` i:

   * `createImageSet`
   * `createAssetSet`
   Tillagt `companyHandle` i:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`
   Tillagt `contextHandle` i:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* IncludeInactive har lagts till i:

   * `getUsers`.
   * `getUserChars`.

* Tillagd `permissionArray` i `createPropertySet`.

* Tillagd `exportJob` i `submitJob`.

**Ändrad**

* In `addUser` and `setUser`, changed `role` to `defaultRole`.

* In `getCompanyMembers`, ändrad `userArray` till `memberArray`.

* In `getCompanyMembership`, ändrad `companyArray` till `membershipArray`.

* In `addUser`, `setCompanyMembership`och `addCompanyMembership`, ändrat `membershipArray` till `companyHandleArray`.

* In `getCompanyMembership`, ändrad `companyArray` till `membershipArray`.

* In `getUserChars`, `includeInvalid` är nu valfritt.

**Borttagen**

* Borttagen `renameFiles` från `renameAsset`.

* Borttagen `getXMPPanelViewDefinition`.
* Borttagen `searchAssetsByFulltext` och `searchAssetsBySimilarity`.

