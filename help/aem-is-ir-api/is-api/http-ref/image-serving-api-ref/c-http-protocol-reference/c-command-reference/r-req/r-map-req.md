---
description: Bildschemadata.
seo-description: Bildschemadata.
seo-title: map
solution: Experience Manager
title: map
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# map{#map}

Bildschemadata.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingReqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> kodning</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

Returnerar `catalog::Map` utan ändring när en enkel katalogpost efterfrågas utan ytterligare angivna kommandon (skalas inte till `catalog::maxPix`).

Om något annat kommando anges i begäran returneras ett sammansatt bildschema, som härleds genom skalning, beskärning, rotering och lagerhantering av alla `catalog::Map`- och/eller `map=`-kommandon som ingår i begäran, precis som bilddata skulle vara med `req=img`.

Ange `text` eller utelämna den andra parametern för att returnera data för bildschemat i form av en `HTML <AREA>`-elementsträng med MIME-svarstyp `text/plain`.

Ange `xml` om du vill formatera svaret som XML i stället för HTML. Textkodning kan anges om så önskas. Standardvärdet är `UTF-8`.

Returnerar en tom sträng (eller ett tomt `<AREA>`-element) om inga mappningsdata hittades för de angivna katalogobjekten och/eller om inga `<AREA>`-element finns kvar efter att bilderna har beskurits.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.

Se [Bildscheman](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
