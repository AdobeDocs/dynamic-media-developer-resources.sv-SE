---
description: Ta bort alla attribut för ett givet s7 elementID.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 0%

---

# deleteAttr{#deleteattr}

Ta bort alla attribut för en given s7:elementID.

`deleteAttr.elementID={attributeName%26attributeName}`

Om ett FXG-nodelement har `s7:elementID` definierat kan attributen för den noden tas bort med det här kommandot.

## Exempel {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

I det här exemplet tas attributen *[!DNL x]*, *[!DNL y]* och *[!DNL visible]* bort från den ursprungliga FXG-noden.
