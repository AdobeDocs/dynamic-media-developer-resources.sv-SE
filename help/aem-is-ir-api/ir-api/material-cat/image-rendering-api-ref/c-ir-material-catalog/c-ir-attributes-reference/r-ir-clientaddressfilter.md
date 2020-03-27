---
description: Klientens IP-adressfilter. Tillåter specifikation av en eller flera IP-adresser eller adressintervall.
seo-description: Klientens IP-adressfilter. Tillåter specifikation av en eller flera IP-adresser eller adressintervall.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

Klientens IP-adressfilter. Tillåter specifikation av en eller flera IP-adresser eller adressintervall.

Om det anges kommer förfrågningar till den här bildkatalogen som kommer från en klient till en IP-adress som inte finns med i listan att avvisas. `localhost` är alltid en implicit del av `ClientAddressFilter` definitionen, även om den inte uttryckligen anges. Förfrågningar som kommer från `localhost` avvisas aldrig, oavsett `ClientAddressFilter` specifikation.

## Egenskaper {#section-21a2992f108d42fb8660c0d65aa61e13}

Kommaavgränsad lista med IP-adresser med valfria netmasker ([CIDR-notation](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) används):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP-adress i *[!DNL ddd.ddd.ddd.ddd]* format

* *[!DNL netmask]* nätmask (0...32)

Det här attributet ignoreras när en förbearbetningsregel med ett `<addressfilter>` element används.

## Standard {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Ärvs från `default::AddressFilter` om inte definierad eller om tom.

## Exempel {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Inga åtkomstbegränsningar: `0.0.0.0/0`
* Bevilja åtkomst till alla adresser som börjar med `192: 192.0.0.0/8`
* Ge åtkomst till de 512 värdarna med adresser mellan `192.168.12.0` och `192.168.13.255: 192.168.12.0/23`

* Ge åtkomst till en enda IP-adress: `192.168.2.117` eller `192.168.2.117/32`

## Se även {#section-6198780c7b3045aabd211eefb38bc565}

[adressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
