---
title: cache
description: Cachekontroll. Möjliggör selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring på den interna [!DNL Platform Server] cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# cache{#cache}

Cachekontroll. Möjliggör selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring på den interna [!DNL Platform Server] cache.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Om bara en `*`cacheControl`*` -värdet anges, det används både på klient- och servercacheminnen.

The `validate` nyckelord gör det möjligt att uppdatera cacheposter när bildfiler har ändrats, utan att behöva vänta på att cacheposten ska upphöra automatiskt. Klientcachning påverkas inte av det här kommandot.

The `update` nyckelord kan användas för att framtvinga uppdatering av cacheposter på serversidan. Detta är användbart efter att resurser har ändrats som inte spåras direkt av cacheminnets valideringsmekanism, till exempel när en teckensnittsfil ändras utan att filnamnet eller det associerade teckensnittets ID ändras.

Om det anges i en kapslad begäran, `cache=on` möjliggör beständig cachelagring på serversidan av bilden som genereras av den kapslade begäran. Försiktighet bör iakttas så att cachelagring för kapslade begäranden endast aktiveras när samma kapslade begäran anropas upprepade gånger med exakt samma parametrar.

## Egenskaper {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Begär attribut. Används oavsett aktuell lagerinställning. Ignoreras när begäran inte returnerar en svarsbild. *`clientControl`*ignoreras när cachelagring på klientsidan inaktiveras av bildkatalogen (om `catalog::Expiration` har ett negativt värde).

Cachekontroll på klientsidan ( `on` och `off` finns även på [!DNL /is/content/].

## Standard {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` för HTTP-begäranden, `cache=off` för kapslade/inbäddade begäranden, `cache=on` för statiska innehållsförfrågningar.

## Se även {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[katalog::Förfallotid](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
