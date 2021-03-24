---
description: Bildstorlek. Pixelstorlek för den högupplösta bilden som katalogsökvägen refererar till.
solution: Experience Manager
title: Storlek
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Storlek{#size}

Bildstorlek. Pixelstorlek för den högupplösta bilden som katalogen refererar till::Path.

Om det här värdet anges används det i Image Serving för att undvika att bilden behöver öppnas för att få den faktiska bildstorleken.

>[!NOTE]
>
>Om `catalog::Size`anges och inte är samma som den faktiska bildstorleken med full upplösning, kan det leda till ett odefinierat beteende.

## Egenskaper {#section-5c914ec8b1444a8e99d811b647cd42a3}

Två heltal, där vart och ett är större än 0, avgränsade med kommatecken. Valfritt.

## Standard {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Om fältet inte finns, eller om fältet är tomt, används bildens faktiska storlek.

## Se även {#section-e63797357d5a4119a10db1e6e088f6e9}

[katalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
