---
description: Ytglansighet Anger materialytans relativa glansighet.
solution: Experience Manager
title: Glans
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# Glans{#gloss}

Ytglansighet Anger materialytans relativa glansighet.

Det här värdet används av renderaren i följande syften:

* Välj belysningskartan när `catalog::Illum` är -1.
* Kontrollerar glanseffekt (speglande reflektion) som återges i samband med `catalog::Type`.
* Styr återgivningseffekter för 3D-reflektion i kombination med `catalog::Type` och `catalog::Roughness`.

## Egenskaper {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Heltal. Procenttal i intervallet 0 till 100. Valfritt för alla material. Används endast för vinjetter med flera reflektionskartor eller vinjetter med 3D-reflektion. Lämna tomt eller ange -1 om det inte är känt eller inte behövs.

## Standard {#section-2352721073524f1a8d461f64a363aac9}

Ett standardvärde anges av vinjetteringen om värdet är -1.

## Se även {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
