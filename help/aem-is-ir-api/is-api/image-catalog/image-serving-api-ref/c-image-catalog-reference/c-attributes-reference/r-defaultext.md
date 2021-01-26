---
description: Standardfilsuffix för bild. Bifogat till fältvärdet för katalogsökvägen (eller katalogsökvägen MaskPath) om sökvägen inte innehåller något filsuffix
seo-description: Standardfilsuffix för bild. Bifogat till fältvärdet för katalogsökvägen (eller katalogsökvägen MaskPath) om sökvägen inte innehåller något filsuffix
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# DefaultExt{#defaultext}

Standardfilsuffix för bild. Bifogat till katalogen::Fältvärdet Sökväg (eller katalog::MaskPath) om sökvägen inte innehåller något filsuffix

Ett filsuffix består av en punkt och ett eller flera tecken mellan punkten och strängens slut. Suffixet läggs till i http-sökvägen om sökvägen inte matchar en katalogpost och om det sista sökvägselementet inte innehåller något filsuffix.

## Egenskaper {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Textsträng. Måste innehålla ett inledande &quot;.&quot; och ett eller flera tecken.

## Standard {#section-1194c36ffe0748c5b9ff7d732a506588}

Ärvs från `default::DefaultExt` om inte definierat. Om det är definierat men tomt tillämpas inget standardsuffix på bildnamn när den här katalogen används.

## Se även {#section-d7c408b979844643adff8258f500eb7c}

[katalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [katalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
