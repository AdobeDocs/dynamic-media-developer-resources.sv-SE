---
description: Standardfilsuffix för bild. Bifogat till fältvärdet för katalogsökvägen (eller katalogsökvägen MaskPath) om sökvägen inte innehåller något filsuffix
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '147'
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
