---
title: IccRenderIntent
description: Färgkonverteringsmetod. Den innehåller standardåtergivningsmetoden för färgkonverteringar när "icc=" inte har angetts för återgivningsmetoden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# IccRenderIntent{#iccrenderintent}

Färgkonverteringsmetod. Anger standardåtergivningsmetod för färgkonverteringar när återgivningsmetoden inte har angetts med `icc=`.

## Egenskaper {#section-2540099fb2fc47d29b04642da4f5922a}

Enum. Ange 0 för perceptuell, 1 för relativ kolorimetri, 2 för mättnad och 3 för absolut kolorimetri.

## Standard {#section-61a05067905b44099c228e15de279dbd}

Ärvs från `default::IccRenderIntent` om den inte är definierad eller om den är tom.

## Se även {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
