---
description: Ange XML som ett s7 elementID.
seo-description: Ange XML som ett s7 elementID.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---


# setElement{#setelement}

Ange XML som ett s7:elementID.

`setElement.elementID=<XML>`

Om ett FXG-nodelement har ett `s7:elementID`-definierat värde ersätts `<XML>`-värdet som ett underordnat element. `<XML>` måste kodas.

## Exempel {#section-f23a998b18994dd3b5d4e1965718db9f}

Anta att ett `s7:elementID="group2"`-attribut är definierat för en `Group`-nod, då gäller följande:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Det här exemplet tar bort alla underordnade noder från `group2`noden och ersätter den med den nya underordnade noden `TextGraphic`.
