---
title: appendElement
description: Lägg till XML i ett s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# appendElement{#appendelement}

Lägg till XML i ett s7:elementID.

`appendElement.elementID=<XML>`

Om ett FXG-nodelement har en `s7:elementID` definierade, `<XML>` värdet läggs till som ett underordnat element. The `<XML>` måste kodas.

## Exempel {#section-4368570aa198485d91b73b4d0741478f}

Anta en `s7:elementID="group1"` -attributet är definierat för en gruppnod och följande är giltigt:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

I det här exemplet läggs ett underordnat textgrafikobjekt till `group1`.
