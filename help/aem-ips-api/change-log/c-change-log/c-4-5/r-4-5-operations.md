---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 4.5.
solution: Experience Manager
title: Nya och ändrade åtgärder
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# Åtgärder: Nytt och ändrat{#operations-new-and-modified}

Beskriver nya och ändrade operationsmetoder för IPS API version 4.5.

Syntax

## Nya åtgärder {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## Ändrade åtgärder {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` innehåller  `animatedGifInfo`,  `swcInfo`,  `cssInfo`och  `javascriptInfo` parametrar.

* `createMetadataField` innehåller en valfri  `isHidden` parameter.

* `saveMetadataField` innehåller en valfri  `isHidden` parameter.

* `searchAssets`
* 
* Parametern `renameFiles` har tagits bort för tidigare versioner och tagits bort från åtgärden `renameAsset`. Sökvägen för den virtuella filen ändras så att den matchar det nya resursnamnet (med filtillägget bevarat), medan sökvägarna för fysiska filer inte påverkas. API-klienter måste ta bort referenser till den här parametern när de uppdaterar till den nya API-versionen.

