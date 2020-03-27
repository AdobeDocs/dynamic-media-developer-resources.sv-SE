---
description: Bilduppsättningsdata från bildkatalogen. Returnerar bilduppsättningsdata för bildkatalogposten som anges i URL-sökvägen.
seo-description: Bilduppsättningsdata från bildkatalogen. Returnerar bilduppsättningsdata för bildkatalogposten som anges i URL-sökvägen.
seo-title: bilduppsättning
solution: Experience Manager
title: bilduppsättning
topic: Scene7 Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bilduppsättning{#imageset}

Bilduppsättningsdata från bildkatalogen. Returnerar bilduppsättningsdata för bildkatalogposten som anges i URL-sökvägen.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingReqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> kodning</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

Innehållet i `catalog::ImageSet` returneras utan ytterligare ändring (förutom stränglokalisering, om tillämpligt), följt av en enda radavslutning (CR/LF). Om URL-sökvägen inte kan tolkas som en giltig katalogpost består svaret endast av en radslutstecken.

Andra kommandon i begärandesträngen ignoreras. HTTP-svaret kan nås med TTL-värdet baserat på `catalog::NonImgExpiration`.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för `req=` parametern:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
