---
description: Bilduppsättningsdata från bildkatalogen. Returnerar bilduppsättningsdata för bildkatalogposten som anges i URL-sökvägen.
solution: Experience Manager
title: bilduppsättning
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# bilduppsättning{#imageset}

Bilduppsättningsdata från bildkatalogen. Returnerar bilduppsättningsdata för bildkatalogposten som anges i URL-sökvägen.

`req=imageset[,text|javascript|{xml[, *`kodning`*]}|{json[&id= *`reqId`*]}]`

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

Innehållet i `catalog::ImageSet` returneras utan ytterligare ändring (utom stränglokalisering, om tillämpligt), följt av en enda radavslutning (CR/LF). Om URL-sökvägen inte kan tolkas som en giltig katalogpost består svaret endast av en radslutstecken.

Andra kommandon i begärandesträngen ignoreras. HTTP-svaret kan nås med TTL-värdet baserat på `catalog::NonImgExpiration`.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standard är `s7jsonResponse`.
