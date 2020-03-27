---
description: Bildstorlek. Pixelstorlek för den högupplösta bilden som katalogsökvägen refererar till.
seo-description: Bildstorlek. Pixelstorlek för den högupplösta bilden som katalogsökvägen refererar till.
seo-title: Storlek
solution: Experience Manager
title: Storlek
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Storlek{#size}

Bildstorlek. Pixelstorlek för den högupplösta bilden som katalogen refererar till::Path.

Om det här värdet anges används det i Image Serving för att undvika att bilden behöver öppnas för att få den faktiska bildstorleken.

>[!NOTE]
>
>Om `catalog::Size`anges och inte är densamma som den faktiska bildstorleken med full upplösning, kan det leda till ett odefinierat beteende.

## Egenskaper {#section-5c914ec8b1444a8e99d811b647cd42a3}

Två heltal, där vart och ett är större än 0, avgränsade med kommatecken. Valfritt.

## Standard {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Om fältet inte finns, eller om fältet är tomt, används bildens faktiska storlek.

## Se även {#section-e63797357d5a4119a10db1e6e088f6e9}

[katalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
