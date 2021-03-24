---
description: Ange ett attribut för ett givet s7 elementID.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# setAttr{#setattr}

Ange ett attribut för ett givet s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Om ett FXG-nodelement har en `s7:elementID` definierad kan du ändra attributen för den noden. Du kan ange så många attribut/värde-par du vill. Attributen behöver inte redan definieras i FXG, men de måste vara giltiga för nodelementet. Alla värden mellan `{}` måste Escaped.

## Exempel {#section-9c37470d5f0349e5b0a97291782cb7a6}

Anta att ett `s7:elementID="Group1"`-attribut är definierat för en `BitmapGraphic`-nod och att följande är giltigt:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

I det här exemplet anges *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* och *[!DNL scaleY]* för `BitmapGraphic` och åsidosätter befintliga värden.
