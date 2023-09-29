---
title: IccRenderIntent
description: Färgkonverteringsmetod. Den innehåller standardåtergivningsmetoden för färgkonverteringar när återgivningsmetoden inte har angetts med "icc=".
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# IccRenderIntent{#iccrenderintent}

Färgkonverteringsmetod. Anger standardåtergivningsmetod för färgkonverteringar när återgivningsmetoden inte har angetts med `icc=`.

## Egenskaper {#section-0a38c60e1525426185616c42824aee2c}

Enum. Ange 0 för perceptuell, 1 för relativ kolorimetri, 2 för mättnad och 3 för absolut kolorimetri. Behåll tomt eller ange ett annat värde så att du kan använda den standardåtergivningsmetod som definierats i färgprofilen.

## Standard {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Ärvs från `default::IccRenderIntent`om inte definierat. Om den är tom används &quot;relativ kolorimetri&quot;.

## Se även {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
