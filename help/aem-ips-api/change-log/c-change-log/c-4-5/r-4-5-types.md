---
description: Beskriver nya och ändrade datatyper för IPS API version 4.5.
seo-description: Beskriver nya och ändrade datatyper för IPS API version 4.5.
seo-title: Datatyper Nytt och ändrat
solution: Experience Manager
title: Datatyper Nytt och ändrat
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Datatyper: Nytt och ändrat{#data-types-new-and-modified}

Beskriver nya och ändrade datatyper för IPS API version 4.5.

Syntax

## Nya typer {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## Ändrade typer {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* Resursen innehåller ett nytt `fileName` fält som returnerar det virtuella filnamnet.
* `AssetSummary` returnerar ett `type` och `name` fält

* `MetadataField` inkluderar `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` kräver ett `urlArray` och lägger till ett valfritt `numUrls` antal

