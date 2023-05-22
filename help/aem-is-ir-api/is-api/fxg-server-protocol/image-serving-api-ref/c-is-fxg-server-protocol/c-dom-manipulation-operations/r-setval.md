---
description: Ange textnodsvärde för s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 0%

---

# setVal{#setval}

Ange textnodsvärde för s7:elementID.

`setVal.elementID= *[!DNL value]*`

Om ett FXG-nodelement har `s7:elementID` kan textvärdet för den noden ändras.

## Exempel {#section-f574fd66dedd4a219aa537d7bdabea23}

Anta en `s7:elementID="paragraph1"` -attribut definieras för en `TextGraphic` och följande gäller:

`&setVal.paragraph=Hello`

I det här exemplet anges textvärdet för styckenoden till&quot;Hello&quot;.
