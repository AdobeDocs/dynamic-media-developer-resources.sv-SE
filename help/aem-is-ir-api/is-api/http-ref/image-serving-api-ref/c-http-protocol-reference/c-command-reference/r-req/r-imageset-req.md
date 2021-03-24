---
description: Bilduppsättningsdata från bildkatalogen. Returnerar bilduppsättningsdata för bildkatalogposten som anges i URL-sökvägen.
solution: Experience Manager
title: bilduppsättning
feature: Dynamic Media Classic,SDK/API,Bilduppsättningar
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# bilduppsättning{#imageset}

Bilduppsättningsdata från bildkatalogen. Returnerar bilduppsättningsdata för bildkatalogposten som anges i URL-sökvägen.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingReqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> kodning</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

Innehållet i `catalog::ImageSet` returneras utan ytterligare ändring (förutom stränglokalisering, om tillämpligt), följt av en enda radavslutning (CR/LF). Om URL-sökvägen inte kan tolkas som en giltig katalogpost består svaret endast av en radslutstecken.

Andra kommandon i begärandesträngen ignoreras. HTTP-svaret kan nås med TTL-värdet baserat på `catalog::NonImgExpiration`.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
