---
description: Adressfilterelement. Valfritt i <rule> och <pathrule> -element.
solution: Experience Manager
title: adressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# adressfilter{#addressfilter}

Adressfilterelement. Valfritt i `<rule>` och `<pathrule>` -element.

Åsidosättningar `attribute::ClientAddressFilter` när regeln används.

## Attribut {#section-31e9ad29e9934933ac154bccbc729172}

Ingen.

## Data {#section-c762bdfe425140d689ea5abf25e9a48a}

Kommaavgränsad lista med IP-adresser. Varje enskild adress kan innehålla ett valfritt netmask-suffix för att tillåta specifikation av IP-adressintervall. Se `attribute::ClientAddressFilter` för mer information.

## Beskrivning {#section-d561b2485e004ef8a2085997d0f4bca6}

Åtkomsten till den här bildkatalogen kan begränsas till en eller flera specifika klient-IP-adresser genom att ange dem i en `<addressfilter>` -element. Ett felmeddelande om att en begäran nekades returneras till klienten om klientens IP-adress inte matchar.

Åtkomsten är inte begränsad om `<addressfilter>` är tom eller inte angiven.

Om `<expression>` i `<rule>` -elementet saknas eller är tomt, `<addressfilter>` tillämpas på alla begäranden.

## Se även {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
