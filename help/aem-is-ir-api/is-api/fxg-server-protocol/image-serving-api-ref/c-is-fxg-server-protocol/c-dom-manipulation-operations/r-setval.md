---
description: Ange textnodsvärde för s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
