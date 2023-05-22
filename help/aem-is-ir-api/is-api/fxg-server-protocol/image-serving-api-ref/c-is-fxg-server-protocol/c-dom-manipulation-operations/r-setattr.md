---
description: Ange ett attribut för ett givet s7 elementID.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# setAttr{#setattr}

Ange ett attribut för ett givet s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Om ett FXG-nodelement har `s7:elementID` kan du ändra attributen för den noden. Du kan ange så många attribut/värde-par du vill. Attributen behöver inte redan definieras i FXG, men de måste vara giltiga för nodelementet. Alla värden däremellan `{}` måste vara Escaped.

## Exempel {#section-9c37470d5f0349e5b0a97291782cb7a6}

Anta en `s7:elementID="Group1"` -attribut definieras för en `BitmapGraphic` nod, gäller följande:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Det här exemplet ställer in *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* och *[!DNL scaleY]* för `BitmapGraphic` och åsidosätter befintliga värden.
