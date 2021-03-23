---
description: Beskriver nya och ändrade datatyper för IPS API version 4.5.
solution: Experience Manager
title: Datatyper Nytt och ändrat
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

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

* Resursen innehåller ett nytt `fileName`-fält som returnerar det virtuella filnamnet.
* `AssetSummary` returnerar ett  `type` och  `name` fält

* `MetadataField` inkluderar  `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` kräver ett  `urlArray` och lägger till ett valfritt  `numUrls` antal

