---
description: Väljare för illustrationsschema. Anger den belysningskarta som materialet ska återges med.
solution: Experience Manager
title: illum
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# illum{#illum}

Väljare för illustrationsschema. Anger den belysningskarta som materialet ska återges med.

`illum=-1|0|1|2`

Om den angivna belysningskartan inte är tillgänglig i målvinjetteringen används den närmaste tillgängliga kartan i stället.

`illum=-1` anger att belysningskartan väljs automatiskt baserat på  `gloss=` värdet.

## Egenskaper {#section-aace8466566e4cf1a0c5a6c0167245c9}

Materialattribut. Ignoreras om vinjetteringen inte definierar flera belysningskartor.

## Standard {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Se även {#section-9132e60381c64aa3a8ed1319690db55e}

[glans=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
