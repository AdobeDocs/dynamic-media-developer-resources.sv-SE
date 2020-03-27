---
description: Väljare för illustrationsschema. Anger den belysningskarta som materialet ska återges med.
seo-description: Väljare för illustrationsschema. Anger den belysningskarta som materialet ska återges med.
seo-title: illum
solution: Experience Manager
title: illum
topic: Scene7 Image Serving - Image Rendering API
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# illum{#illum}

Väljare för illustrationsschema. Anger den belysningskarta som materialet ska återges med.

`illum=-1|0|1|2`

Om den angivna belysningskartan inte är tillgänglig i målvinjetteringen används den närmaste tillgängliga kartan i stället.

`illum=-1` anger att belysningskartan väljs automatiskt baserat på `gloss=` värdet.

## Egenskaper {#section-aace8466566e4cf1a0c5a6c0167245c9}

Materialattribut. Ignoreras om vinjetteringen inte definierar flera belysningskartor.

## Standard {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Se även {#section-9132e60381c64aa3a8ed1319690db55e}

[glans=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
