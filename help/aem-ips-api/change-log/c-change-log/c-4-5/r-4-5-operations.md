---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 4.5.
solution: Experience Manager
title: Nya och ändrade åtgärder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: d2e73ae5f92d9ba3471dc7207842753ccff94c28
workflow-type: tm+mt
source-wordcount: '103'
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
* Parametern `renameFiles` har tagits bort för tidigare versioner och tagits bort från åtgärden `renameAsset`. Sökvägen för den virtuella filen ändras så att den matchar det nya resursnamnet (med filtillägget bevarat), medan sökvägarna för fysiska filer inte påverkas. API-klienter måste ta bort referenser till den här parametern när de uppdaterar till den nya API-versionen.
