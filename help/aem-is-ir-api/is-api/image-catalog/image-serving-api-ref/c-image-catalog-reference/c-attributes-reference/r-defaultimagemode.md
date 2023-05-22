---
description: Standardbildläge. Väljer hur standardbilden ska användas när det inte går att hitta de bilder som har angetts i begäran.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# DefaultImageMode{#defaultimagemode}

Standardbildläge. Väljer hur standardbilden ska användas när det inte går att hitta de bilder som har angetts i begäran.

## Egenskaper {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &#39;0&#39; om du vill ersätta hela den sammansatta bilden, även om den saknade bilden bara är ett av flera lager, &#39;1&#39; om du vill ersätta varje lagrets källbild som saknas med standardbilden och returnera den sammansatta bilden som vanligt.

## Begränsningar {#section-04cb0d50e8914564a8d226d0d4663c8b}

Bildservning återgår till `DefaultImageMode=0` vid bildåtergivning, FXG eller `req=set` begäranden misslyckas.

## Standard {#section-9e318524a2a5496386901286748c7ee7}

Ärvs från `default::DefaultImage` om den inte är definierad eller om den är tom.

## Se även {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
