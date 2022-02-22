---
title: illum
description: Väljare för illustrationsschema. Anger den belysningskarta som materialet ska återges med.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# illum{#illum}

Väljare för illustrationsschema. Anger den belysningskarta som materialet ska återges med.

`illum=-1|0|1|2`

Om den angivna belysningskartan inte är tillgänglig i målvinjetteringen används den närmaste tillgängliga kartan i stället.

`illum=-1` Anger att belysningskartan väljs automatiskt baserat på `gloss=` värde.

## Egenskaper {#section-aace8466566e4cf1a0c5a6c0167245c9}

Materialattribut. Ignoreras om vinjetteringen inte definierar flera belysningskartor.

## Standard {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Se även {#section-9132e60381c64aa3a8ed1319690db55e}

[glans=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
