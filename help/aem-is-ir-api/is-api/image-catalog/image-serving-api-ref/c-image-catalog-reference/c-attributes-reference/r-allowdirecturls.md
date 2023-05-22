---
description: Tillåt absoluta URL:er som bildkällor.
solution: Experience Manager
title: AllowDirectUrls
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e160101a-9bb7-452f-b892-c2aa65e26e94
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 0%

---

# AllowDirectUrls{#allowdirecturls}

Tillåt absoluta URL:er som bildkällor.

Aktiverar eller inaktiverar stöd för inbäddade absoluta URL:er i `src=` och `mask=` kommandon. När det är inaktiverat är det bara URL:er som är relativa till `attribute::RootUrl` är tillåtna.

## Egenskaper {#section-192825a6b02e4cc4a6aa102f93be89f0}

Flagga.

## Standard {#section-c2eb9ab424db41c6aac91ba2cbe00ef5}

Ärvs från `default::AllowDirectUrls` om den inte är definierad eller om den är tom.

## Se även {#section-604f9500749c4e1a968b260b9a3812b2}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::RootUrl](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137)
