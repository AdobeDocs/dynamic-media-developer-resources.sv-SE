---
description: Användardata från bildkatalog. Returnerar användardata för bildkatalogposten som anges i URL-sökvägen.
seo-description: Användardata från bildkatalog. Returnerar användardata för bildkatalogposten som anges i URL-sökvägen.
seo-title: användardata
solution: Experience Manager
title: användardata
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# användardata{#userdata}

Användardata från bildkatalog. Returnerar användardata för bildkatalogposten som anges i URL-sökvägen.

`req=userdata[,text|{xml[, *`kodning`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> kodning</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Innehållet i `catalog::UserData` returneras. När formatet &quot;text&quot; anges ersätts alla instanser av `??` i `catalog::UserData`med radavslutare, och en radslutstecken (CR/LF) läggs till i slutet. Om URL-sökvägen inte kan tolkas som en giltig katalogpost består svaret endast av en radslutstecken. Lämplig formatering används när formatet &#39;xml&#39; eller &#39;json&#39; begärs.

Andra kommandon i begärandesträngen ignoreras.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.

>[!NOTE]
>
>Kolontecknet tillåts inte i nyckelnamn för användardataegenskaper.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
