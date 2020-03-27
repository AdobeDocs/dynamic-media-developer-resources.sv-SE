---
description: Adressfilterelement. Valfritt i <rule>-element. Åsidosätter attributet ClientAddressFilter när regeln används.
seo-description: Adressfilterelement. Valfritt i <rule>-element. Åsidosätter attributet ClientAddressFilter när regeln används.
seo-title: adressfilter
solution: Experience Manager
title: adressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# adressfilter{#addressfilter}

Adressfilterelement. Valfritt i `<rule>` element. Åsidosätter attribut::ClientAddressFilter när regeln används.

## Attribut {#section-e7a0960f7f0045da91de37824aa4aeaa}

Ingen.

## Data {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Kommaavgränsad lista med IP-adresser. Varje enskild adress kan innehålla ett valfritt netmask-suffix för att tillåta specifikation av IP-adressintervall. Mer information finns ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` i.

## Beskrivning {#section-099b7839c4be40c68cbff29dad14e7d5}

Åtkomsten till den här bildkatalogen kan begränsas till en eller flera specifika IP-adresser genom att ange dem i ett `<addressfilter>` element. Ett felmeddelande om att en begäran nekades returneras till klienten om klientens IP-adress inte matchar.

Åtkomsten är inte begränsad om `<addressfilter>` den är tom eller inte har angetts.

Om elementet `<expression>` i `<rule>` inte finns eller är tomt `<addressfilter>` tillämpas det på alla begäranden.

`localhost` är alltid en implicit del av `ClientAddressFilter` definitionen, även om den inte uttryckligen anges. Förfrågningar som kommer från `localhost` avvisas aldrig, oavsett `ClientAddressFilter` specifikation.

## SeeaÄven {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
