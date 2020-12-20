---
description: Lägg till XML i ett s7 elementID.
seo-description: Lägg till XML i ett s7 elementID.
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---


# appendElement{#appendelement}

Lägg till XML i ett s7:elementID.

`appendElement.elementID=<XML>`

Om ett FXG-nodelement har ett `s7:elementID`-definierat värde läggs `<XML>`-värdet till som ett underordnat element. `<XML>` måste kodas.

## Exempel {#section-4368570aa198485d91b73b4d0741478f}

Anta att ett `s7:elementID="group1"`-attribut har definierats för en gruppnod, då gäller följande:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

I det här exemplet läggs en underordnad textbild till `group1`.
