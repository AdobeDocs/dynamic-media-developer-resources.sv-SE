---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 6.
solution: Experience Manager
title: Nya och ändrade åtgärder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
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

* Tillagd `isHidden` och `initialTagValue` till:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Tillagd `thumbAssetHandle` till:

   * `createImageSet`
   * `createAssetSet`

   Tillagd `companyHandle` till:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   Tillagd `contextHandle` till:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* IncludeInactive har lagts till i:

   * `getUsers`.
   * `getUserChars`.

* Tillagd `permissionArray` till `createPropertySet`.

* Tillagd `exportJob` till `submitJob`.

**Ändrad**

* I `addUser` och `setUser`, ändrat `role` till `defaultRole`.

* I `getCompanyMembers`, ändrat `userArray` till `memberArray`.

* I `getCompanyMembership`, ändrat `companyArray` till `membershipArray`.

* I `addUser`, `setCompanyMembership`och `addCompanyMembership`, ändrat `membershipArray` till `companyHandleArray`.

* I `getCompanyMembership`, ändrat `companyArray` till `membershipArray`.

* I `getUserChars`, `includeInvalid` är nu valfritt.

**Borttagen**

* Borttagen `renameFiles` från `renameAsset`.

* Borttagen `getXMPPanelViewDefinition`.
* Borttagen `searchAssetsByFulltext` och `searchAssetsBySimilarity`.
