---
description: Standardbildläge. Väljer hur standardbilden ska användas när det inte går att hitta de bilder som har angetts i begäran.
seo-description: Standardbildläge. Väljer hur standardbilden ska användas när det inte går att hitta de bilder som har angetts i begäran.
seo-title: DefaultImageMode
solution: Experience Manager
title: DefaultImageMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e5640f09-e1e3-473b-8fbc-84c6bfce2460
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# DefaultImageMode{#defaultimagemode}

Standardbildläge. Väljer hur standardbilden ska användas när det inte går att hitta de bilder som har angetts i begäran.

## Egenskaper {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &#39;0&#39; om du vill ersätta hela den sammansatta bilden, även om den saknade bilden bara är ett av flera lager, &#39;1&#39; om du vill ersätta varje lagrets källbild som saknas med standardbilden och returnera den sammansatta bilden som vanligt.

## Begränsningar {#section-04cb0d50e8914564a8d226d0d4663c8b}

Bildservern återgår till `DefaultImageMode=0` när en kapslad bildåtergivning, FXG eller `req=set`-begäranden misslyckas.

## Standard {#section-9e318524a2a5496386901286748c7ee7}

Ärvs från `default::DefaultImage` om det inte är definierat eller om det är tomt.

## Se även {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
