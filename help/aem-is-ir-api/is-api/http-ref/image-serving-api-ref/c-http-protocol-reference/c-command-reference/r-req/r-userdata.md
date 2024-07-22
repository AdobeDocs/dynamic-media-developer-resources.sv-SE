---
description: Användardata från bildkatalog. Returnerar användardata för bildkatalogposten som anges i URL-sökvägen.
solution: Experience Manager
title: användardata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# användardata{#userdata}

Användardata från bildkatalog. Returnerar användardata för bildkatalogposten som anges i URL-sökvägen.

`req=userdata[,text|{xml[, *`kodning`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">-kodning</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Innehållet i `catalog::UserData` returneras. När formatet &quot;text&quot; har angetts ersätts alla instanser av `??` i `catalog::UserData` av radavslutningar och en enkelradsterminator (CR/LF) läggs till i slutet. Om URL-sökvägen inte kan tolkas som en giltig katalogpost består svaret endast av en radslutstecken. Lämplig formatering används när formatet &#39;xml&#39; eller &#39;json&#39; begärs.

Andra kommandon i begärandesträngen ignoreras.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.

>[!NOTE]
>
>Kolontecknet tillåts inte i nyckelnamn för användardataegenskaper.

Begäranden som har stöd för JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
