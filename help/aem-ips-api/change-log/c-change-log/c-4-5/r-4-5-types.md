---
description: Beskriver nya och ändrade datatyper för IPS API version 4.5.
solution: Experience Manager
title: Datatyper Nytt och ändrat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# Datatyper: Ny och ändrad{#data-types-new-and-modified}

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
* `AssetSummary` returnerar ett `type`- och `name`-fält

* `MetadataField` innehåller `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` kräver en `urlArray` och lägger till ett valfritt `numUrls`-antal
