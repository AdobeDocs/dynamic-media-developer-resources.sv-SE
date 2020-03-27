---
description: Adressfilterelement. Valfritt i elementen <rule> och <pathrule>.
seo-description: Adressfilterelement. Valfritt i elementen <rule> och <pathrule>.
seo-title: adressfilter
solution: Experience Manager
title: adressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# adressfilter{#addressfilter}

Adressfilterelement. Valfritt i `<rule>` och `<pathrule>` element.

Åsidosätter `attribute::ClientAddressFilter` när regeln används.

## Attribut {#section-31e9ad29e9934933ac154bccbc729172}

Ingen.

## Data {#section-c762bdfe425140d689ea5abf25e9a48a}

Kommaavgränsad lista med IP-adresser. Varje enskild adress kan innehålla ett valfritt netmask-suffix för att tillåta specifikation av IP-adressintervall. Mer information finns `attribute::ClientAddressFilter` i.

## Beskrivning {#section-d561b2485e004ef8a2085997d0f4bca6}

Åtkomsten till den här bildkatalogen kan begränsas till en eller flera specifika klient-IP-adresser genom att ange dem i ett `<addressfilter>` element. Ett felmeddelande om att en begäran nekades returneras till klienten om klientens IP-adress inte matchar.

Åtkomsten är inte begränsad om `<addressfilter>` den är tom eller inte har angetts.

Om elementet `<expression>` i `<rule>` inte finns eller är tomt `<addressfilter>` tillämpas det på alla begäranden.

## Se även {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
