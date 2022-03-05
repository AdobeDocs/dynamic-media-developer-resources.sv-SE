---
description: Klientens IP-adressfilter. Tillåter specifikation av en eller flera IP-adresser eller adressintervall.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# ClientAddressFilter{#clientaddressfilter}

Klientens IP-adressfilter. Tillåter specifikation av en eller flera IP-adresser eller adressintervall.

När det anges avvisas begäranden till den här bildkatalogen som kommer från en klient till en IP-adress som inte finns med i listan.

## Egenskaper {#section-d785265988324af68835410c9ba54147}

Kommaavgränsad lista med IP-adresser med valfria netmasker (CIDR-notation används):

`*`ipAddress`*` `[`/ *`netmask`*`]`* `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>IP-adress i <span class="varname"> ddd.ddd.ddd.ddd</span> format. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>Nätmask (0...32). </p></td> 
 </tr> 
</table>

Det här attributet ignoreras när en förbearbetningsregel med en `<addressfilter>` -element används.

## Standard {#section-de26e8c9225745e985e4beac1f03f4f6}

Ärvs från `default::AddressFilter` om den inte är definierad eller om den är tom.

## Exempel {#section-a955314d2b6a4213a16c12a8b18d8627}

Inga åtkomstbegränsningar: `0.0.0.0/0`

Bevilja åtkomst till alla adresser från och med 192: `192.0.0.0/8`

Ge åtkomst till de 512 värdarna med adresser mellan 192.168.12.0 och 192.168.13.255: `192.168.12.0/23`

Ge åtkomst till en enda IP-adress: `192.168.2.117` eller `192.168.2.117/32`

## Se även {#section-4ea89a7d82e14a4a800487d2d8801465}

[adressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
