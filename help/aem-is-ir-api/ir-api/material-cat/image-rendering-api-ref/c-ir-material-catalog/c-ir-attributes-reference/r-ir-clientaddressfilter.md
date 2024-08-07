---
title: ClientAddressFilter
description: Klientens IP-adressfilter. Tillåter specifikation av en eller flera IP-adresser eller adressintervall.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# ClientAddressFilter{#clientaddressfilter}

Klientens IP-adressfilter. Tillåter specifikation av en eller flera IP-adresser eller adressintervall.

När det anges avvisas begäranden till den här bildkatalogen som kommer från en klient till en IP-adress som inte finns med i listan. `localhost` är alltid implicit en del av definitionen `ClientAddressFilter`, även om den inte uttryckligen anges. Begäranden som kommer från `localhost` nekas aldrig, oavsett specifikationen för `ClientAddressFilter`.

## Egenskaper {#section-21a2992f108d42fb8660c0d65aa61e13}

Kommaavgränsad lista med IP-adresser med valfria netmasker ([CIDR-notation](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) används):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP-adress i formatet *[!DNL ddd.ddd.ddd.ddd]*

* *[!DNL netmask]* nätmask (0...32)

Det här attributet ignoreras när en förbearbetningsregel med ett `<addressfilter>`-element används.

## Standard {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Ärvs från `default::AddressFilter` om inte definierad eller om tom.

## Exempel {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Inga åtkomstbegränsningar: `0.0.0.0/0`
* Bevilja åtkomst till alla adresser med början från `192: 192.0.0.0/8`
* Bevilja åtkomst till de 512 värdarna med adresser mellan `192.168.12.0` och `192.168.13.255: 192.168.12.0/23`

* Bevilja åtkomst till en enskild IP-adress: `192.168.2.117` eller `192.168.2.117/32`

## Se även {#section-6198780c7b3045aabd211eefb38bc565}

[adressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
