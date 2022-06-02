---
description: Adressfilterelement. Valfritt i <rule> -element. Åsidosätter attributet ClientAddressFilter när regeln används.
solution: Experience Manager
title: adressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# adressfilter{#addressfilter}

Adressfilterelement. Valfritt i `<rule>` -element. Åsidosätter attribut::ClientAddressFilter när regeln används.

## Attribut {#section-e7a0960f7f0045da91de37824aa4aeaa}

Ingen.

## Data {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Kommaavgränsad lista med IP-adresser. Varje enskild adress kan innehålla ett valfritt netmask-suffix för att tillåta specifikation av IP-adressintervall. Se [attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) för mer information.

## Beskrivning {#section-099b7839c4be40c68cbff29dad14e7d5}

Åtkomsten till den här bildkatalogen kan begränsas till en eller flera specifika IP-adresser genom att ange dem i en `<addressfilter>` -element. Ett felmeddelande om att en begäran nekades returneras till klienten om klientens IP-adress inte matchar.

Åtkomsten är inte begränsad om `<addressfilter>` är tom eller inte angiven.

Om `<expression>` i `<rule>` -elementet saknas eller är tomt, `<addressfilter>` tillämpas på alla begäranden.

`localhost` är alltid implicit en del av `ClientAddressFilter` definition, även om den inte uttryckligen anges. Begäranden från `localhost` avvisas aldrig, oavsett `ClientAddressFilter` -specifikation.

## SeeaÄven {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
