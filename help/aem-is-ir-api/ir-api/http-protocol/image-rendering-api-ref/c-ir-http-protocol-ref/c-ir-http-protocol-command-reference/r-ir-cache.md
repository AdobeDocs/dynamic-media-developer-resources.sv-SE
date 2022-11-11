---
title: cache
description: Cachekontroll. Möjliggör selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring på den interna [!DNL Platform Server] cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# cache {#cache}

Cachekontroll. Gör att du kan inaktivera cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring på den interna [!DNL Platform Server] cache.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>på | av | validera </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>på | av </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>på | av </p></td> 
 </tr> 
</table>

Om bara en *`cacheControl`* -värdet anges, det används både på klient- och servercacheminnen.

The `validate`Nyckelordet tillåter uppdatering av servercacheposter efter att textur- eller vinjettfiler har ändrats, utan att du behöver vänta på att cacheposten ska upphöra automatiskt. Klientcachning påverkas inte av det här kommandot.

Om det anges i en kapslad begäran, `cache=on` möjliggör beständig cachelagring på serversidan av bilden som genereras av den kapslade begäran. Se till att du bara aktiverar cachelagring för kapslade begäranden när samma kapslade begäran anropas upprepade gånger med samma parametrar.

## Egenskaper {#section-0dcbd62e1122400e8c347f408f2d937e}

Kan förekomma var som helst i begäran. Ignoreras när begäran inte returnerar en svarsbild. Egenskapen *`clientControl`* ignoreras när cachelagring på klientsidan inaktiveras av materialkatalogen (om `attribute::Expiration` har ett negativt värde). Egenskapen *`serverControl`* ignoreras om servercachning är inaktiverad ( `PlatformServer::cache.enable`).

## Standard {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` För HTTP-begäranden `cache=off` för kapslade/inbäddade begäranden.

## Se även {#section-2f5853751dab49579e97418fa766bdf9}

[katalog::Förfallotid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
