---
description: Ytglansighet Anger materialytans relativa glansighet.
seo-description: Ytglansighet Anger materialytans relativa glansighet.
seo-title: Glans
solution: Experience Manager
title: Glans
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Glans{#gloss}

Ytglansighet Anger materialytans relativa glansighet.

Det här värdet används av renderaren i följande syften:

* Markera belysningskartan när `catalog::Illum` är -1.
* Styr glanseffekten (speglande reflektion) som återges tillsammans med `catalog::Type`.
* Styr återgivningseffekter för 3D-reflektion i samband med `catalog::Type` och `catalog::Roughness`.

## Egenskaper {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Heltal. Procenttal i intervallet 0 till 100. Valfritt för alla material. Används endast för vinjetter med flera reflektionskartor eller vinjetter med 3D-reflektion. Lämna tomt eller ange -1 om det inte är känt eller inte behövs.

## Standard {#section-2352721073524f1a8d461f64a363aac9}

Ett standardvärde anges av vinjetteringen om värdet är -1.

## Se även {#section-0213bbdb7d6d4974a7c53822957717c1}

[glans=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [katalog::grovhet](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99),  [katalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
