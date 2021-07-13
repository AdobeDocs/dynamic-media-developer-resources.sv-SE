---
description: Bilden finns.
solution: Experience Manager
title: exists
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# exists{#exists}

Bilden finns.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* unik begärandeidentifierare

Returnerar en enda egenskap med namnet `catalogRecord.exists`. Egenskapsvärdet anges till &quot;1&quot; om den angivna katalogposten finns i bilden eller standardkatalogen, och i annat fall är värdet &quot;0&quot;. `req=exists` begäranden mot  `/is/content` kontexten indikerar om det finns en angiven post i den statiska innehållskatalogen eller inte.

Andra kommandon i begärandesträngen ignoreras. HTTP-svaret kan nås med TTL-värdet baserat på `attribute::NonImgExpiration`.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
