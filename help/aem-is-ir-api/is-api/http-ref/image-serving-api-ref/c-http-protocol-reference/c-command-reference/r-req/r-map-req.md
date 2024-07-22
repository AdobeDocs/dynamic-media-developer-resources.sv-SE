---
title: map
description: Bildschemadata.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# map{#map}

Bildschemadata.

`req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">-kodning</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

Returnerar `catalog::Map` utan ändring när en enkel katalogpost efterfrågas utan ytterligare kommandon angivna (skalas inte till `catalog::maxPix`).

Om något annat kommando anges i begäran returneras ett sammansatt bildschema. Det sammansatta bildschemat härleds genom att alla `catalog::Map`- och/eller `map=` -kommandon som ingår i begäran skalas, beskärs, roteras och läggs i lager, precis som bilddata skulle vara med `req=img`.

Ange `text` eller utelämna den andra parametern så att du kan returnera data för bildschemat i form av en `HTML <AREA>` -elementsträng med MIME-svarstyp `text/plain`.

Ange `xml` så att du kan formatera svaret som XML i stället för HTML. Textkodning kan anges om så önskas. Standardvärdet är `UTF-8`.

Returnerar en tom sträng (eller ett tomt `<AREA>`-element) om inga mappningsdata hittades för de angivna katalogobjekten och/eller om inga `<AREA>` -element återstår efter att bilderna har beskurits.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.

Begäranden som har stöd för JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.

Se [Bildscheman](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
