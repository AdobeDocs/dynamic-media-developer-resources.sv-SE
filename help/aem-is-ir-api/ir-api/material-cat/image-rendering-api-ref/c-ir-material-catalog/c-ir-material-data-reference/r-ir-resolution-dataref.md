---
description: Upplösning. Bildupplösningen "Real-world", som vanligen uttrycks som pixlar per tum, men kan också finnas i andra enheter, t.ex. pixlar per meter.
seo-description: Upplösning. Bildupplösningen "Real-world", som vanligen uttrycks som pixlar per tum, men kan också finnas i andra enheter, t.ex. pixlar per meter.
seo-title: Upplösning
solution: Experience Manager
title: Upplösning
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 281c7ff6-8f78-4654-98ec-0db4299b80d9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Upplösning{#resolution}

Upplösning. Bildupplösningen &quot;Real-world&quot;, som vanligen uttrycks som pixlar per tum, men kan också finnas i andra enheter, t.ex. pixlar per meter.

## Egenskaper {#section-985ca2ad858c4e9c9cbb303f55447553}

Reellt tal, större än 0. Krävs för textur- och dekala material, såvida inte bildupplösningen är samma som attributet::Upplösning. Ignoreras av heltäckande färg och kabinettmaterial.

## Standard {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` används om fältet inte finns, om värdet är 0 eller negativt eller om fältet är tomt.

## Se även {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
