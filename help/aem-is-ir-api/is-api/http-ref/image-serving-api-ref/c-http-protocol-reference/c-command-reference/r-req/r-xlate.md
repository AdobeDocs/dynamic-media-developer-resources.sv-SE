---
description: Tillgängliga språkspecifika versioner. Returnerar en lista med tillgängliga språkspecifika versioner av det katalog-ID som anges i sökvägen för begäran.
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---


# xlate{#xlate}

Tillgängliga språkspecifika versioner. Returnerar en lista med tillgängliga språkspecifika versioner av det katalog-ID som anges i sökvägen för begäran.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

Se [Översättning av objekt-ID](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Exempel:

`xlate.translatedIds=image,image_fr,image_de`

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
