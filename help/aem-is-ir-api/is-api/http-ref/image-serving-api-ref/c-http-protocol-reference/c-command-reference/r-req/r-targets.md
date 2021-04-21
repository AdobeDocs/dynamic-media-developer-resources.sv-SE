---
description: Zoomningen anger data från bildkatalogen som mål. Returnerar zoommåldata för bildkatalogposten som anges i URL-sökvägen.
solution: Experience Manager
title: mål
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# mål{#targets}

Zoomningen anger data från bildkatalogen som mål. Returnerar zoommåldata för bildkatalogposten som anges i URL-sökvägen.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingReqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> kodning</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

Innehållet i `catalog::Targets` returneras. När formatet text begärs ersätts alla instanser av `??` i `catalog::Targets` av radavslutare och en radavslutare ( `CR/LF`) läggs till i slutet. Om URL-sökvägen inte kan tolkas som en giltig katalogpost består svaret endast av en radslutstecken. Lämplig formatering används när formatet &#39;xml&#39; eller &#39;json&#39; begärs.

Andra kommandon i begärandesträngen ignoreras.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
