---
title: setVal
description: Ange textnodsvärdet för s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# setVal{#setval}

Ange textnodsvärdet för s7:elementID.

`setVal.elementID= *[!DNL value]*`

Om ett FXG-nodelement har en `s7:elementID` kan textvärdet för den noden ändras.

## Exempel {#section-f574fd66dedd4a219aa537d7bdabea23}

Anta en `s7:elementID="paragraph1"` -attribut definieras för en `TextGraphic` och följande gäller:

`&setVal.paragraph=Hello`

I det här exemplet anges textvärdet för styckenoden till&quot;Hello&quot;.
