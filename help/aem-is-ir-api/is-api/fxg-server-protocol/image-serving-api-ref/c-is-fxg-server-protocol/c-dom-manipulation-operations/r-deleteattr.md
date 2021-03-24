---
description: Ta bort alla attribut för ett givet s7 elementID.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---


# deleteAttr{#deleteattr}

Ta bort alla attribut för ett givet s7:elementID.

`deleteAttr.elementID={attributeName%26attributeName}`

Om ett FXG-nodelement har ett `s7:elementID`-definierat, kan attributen för den noden tas bort med det här kommandot.

## Exempel {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

I det här exemplet tas attributen *[!DNL x]*, *[!DNL y]* och *[!DNL visible]* bort från den ursprungliga FXG-noden.
