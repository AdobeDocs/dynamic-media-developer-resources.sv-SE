---
description: Ange textnodsvärde för s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# setVal{#setval}

Ange textnodsvärde för s7:elementID.

`setVal.elementID= *[!DNL value]*`

Om ett FXG-nodelement har en `s7:elementID`-definition kan textvärdet för den noden ändras.

## Exempel {#section-f574fd66dedd4a219aa537d7bdabea23}

Anta att ett `s7:elementID="paragraph1"`-attribut är definierat för en `TextGraphic`-nod, då gäller följande:

`&setVal.paragraph=Hello`

I det här exemplet anges textvärdet för styckenoden till&quot;Hello&quot;.
