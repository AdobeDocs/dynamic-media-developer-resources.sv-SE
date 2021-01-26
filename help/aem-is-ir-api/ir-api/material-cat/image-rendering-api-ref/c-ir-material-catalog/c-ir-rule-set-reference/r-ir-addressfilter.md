---
description: Adressfilterelement. Valfritt i <rule>-element. Åsidosätter attributet ClientAddressFilter när regeln används.
seo-description: Adressfilterelement. Valfritt i <rule>-element. Åsidosätter attributet ClientAddressFilter när regeln används.
seo-title: adressfilter
solution: Experience Manager
title: adressfilter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# adressfilter{#addressfilter}

Adressfilterelement. Valfritt i `<rule>`-element. Åsidosätter attribut::ClientAddressFilter när regeln används.

## Attribut {#section-e7a0960f7f0045da91de37824aa4aeaa}

Ingen.

## Data {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Kommaavgränsad lista med IP-adresser. Varje enskild adress kan innehålla ett valfritt netmask-suffix för att tillåta specifikation av IP-adressintervall. Mer information finns i ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`.

## Beskrivning {#section-099b7839c4be40c68cbff29dad14e7d5}

Åtkomsten till den här bildkatalogen kan begränsas till en eller flera specifika IP-adresser genom att ange dem i ett `<addressfilter>`-element. Ett felmeddelande om att en begäran nekades returneras till klienten om klientens IP-adress inte matchar.

Åtkomsten är inte begränsad om `<addressfilter>` är tom eller inte har angetts.

Om `<expression>`-elementet i `<rule>` saknas eller är tomt tillämpas `<addressfilter>` på alla begäranden.

`localhost` är alltid en implicit del av  `ClientAddressFilter` definitionen, även om den inte uttryckligen anges. Begäranden som kommer från `localhost` avvisas aldrig, oavsett `ClientAddressFilter`-specifikationen.

## SeeaÄven {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
