---
title: setElement
description: Ange XML som ett s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---

# setElement{#setelement}

Ange XML som ett s7:elementID.

`setElement.elementID=<XML>`

Om ett FXG-nodelement har en `s7:elementID` definierade, `<XML>` värdet ersätts som ett underordnat element. The `<XML>` måste kodas.

## Exempel {#section-f23a998b18994dd3b5d4e1965718db9f}

Anta en `s7:elementID="group2"` -attribut definieras för en `Group` och följande gäller:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Det här exemplet tar bort alla underordnade objekt från `group2`nod och ersätter den med nytt `TextGraphic` underordnad nod.
