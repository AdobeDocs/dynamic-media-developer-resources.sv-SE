---
description: Ange attribut till FXG-rotelementet.
solution: Experience Manager
title: setAttr.rootElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 47bd947f-c078-4fd3-99cb-5ef48ea3e05e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 0%

---

# setAttr.rootElement{#setattr-rootelement}

Ange attribut till FXG-rotelementet.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

Det här kommandot kan ändra attribut för rotelementet.

## Exempel {#section-2758a6e316c34b99b13b02147e5973bb}

Om vi har följande rotelement:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

När du har använt följande kommando:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

Rotelementet har ändrats till följande:

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
