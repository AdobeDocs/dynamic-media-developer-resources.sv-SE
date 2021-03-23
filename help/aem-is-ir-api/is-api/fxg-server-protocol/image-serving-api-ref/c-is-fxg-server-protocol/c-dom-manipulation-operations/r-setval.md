---
description: Ange textnodsvärde för s7 elementID.
seo-description: Ange textnodsvärde för s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
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
