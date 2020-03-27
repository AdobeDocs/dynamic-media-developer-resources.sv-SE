---
description: Bilden finns.
seo-description: Bilden finns.
seo-title: exists
solution: Experience Manager
title: exists
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# exists{#exists}

Bilden finns.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* unik begärandeidentifierare

Returnerar en enda egenskap med namnet `catalogRecord.exists`. Egenskapsvärdet anges till &quot;1&quot; om den angivna katalogposten finns i bilden eller standardkatalogen, och i annat fall är värdet &quot;0&quot;. `req=exists` begäranden mot `/is/content` kontexten indikerar om det finns en angiven post i den statiska innehållskatalogen eller inte.

Andra kommandon i begärandesträngen ignoreras. HTTP-svaret kan nås med TTL-värdet baserat på `attribute::NonImgExpiration`.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för `req=` parametern:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
