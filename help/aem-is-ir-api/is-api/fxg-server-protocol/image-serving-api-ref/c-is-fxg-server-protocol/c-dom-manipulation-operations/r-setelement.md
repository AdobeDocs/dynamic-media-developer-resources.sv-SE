---
description: Ange XML som ett s7 elementID.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
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
