---
description: Bilden finns.
solution: Experience Manager
title: exists
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# exists{#exists}

Bilden finns.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* unik begärandeidentifierare

Returnerar en enskild egenskap med namnet `catalogRecord.exists`. Egenskapsvärdet anges till &quot;1&quot; om den angivna katalogposten finns i bilden eller standardkatalogen, och i annat fall är värdet &quot;0&quot;. `req=exists` förfrågningar mot `/is/content`-kontexten indikerar om en angiven post finns eller inte i den statiska innehållskatalogen.

Andra kommandon i begärandesträngen ignoreras. HTTP-svaret kan nås med TTL-värdet baserat på `attribute::NonImgExpiration`.

Begäranden som har stöd för JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
