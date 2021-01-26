---
description: Cachekontroll. Tillåter selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring i den interna plattformsservercachen.
seo-description: Cachekontroll. Tillåter selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring i den interna plattformsservercachen.
seo-title: cache
solution: Experience Manager
title: cache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# cache{#cache}

Cachekontroll. Tillåter selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring i den interna plattformsservercachen.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>på | av | validera </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>på | av </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>på | av </p></td> 
 </tr> 
</table>

Om bara ett *`cacheControl`*-värde har angetts tillämpas det på både klient- och servercachen.

Nyckelordet `validate` tillåter uppdatering av servercacheposter efter att textur- eller vinjettfiler har ändrats, utan att du behöver vänta på att cacheposten ska upphöra automatiskt. Klientcachning påverkas inte av det här kommandot.

Om `cache=on` anges i en kapslad begäran aktiveras beständig cachelagring på serversidan av bilden som genereras av den kapslade begäran. Försiktighet bör iakttas så att cachelagring för kapslade begäranden endast aktiveras när samma kapslade begäran anropas upprepade gånger med exakt samma parametrar.

## Egenskaper {#section-0dcbd62e1122400e8c347f408f2d937e}

Kan förekomma var som helst i begäran. Ignoreras när begäran inte returnerar en svarsbild. *`clientControl`* ignoreras när cachelagring på klientsidan inaktiveras av materialkatalogen (om  `attribute::Expiration` det har ett negativt värde). *`serverControl`* ignoreras om servercachning är inaktiverad (  `PlatformServer::cache.enable`).

## Standard {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` för HTTP-begäranden,  `cache=off` för kapslade/inbäddade begäranden.

## Se även {#section-2f5853751dab49579e97418fa766bdf9}

[katalog::Förfallotid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
