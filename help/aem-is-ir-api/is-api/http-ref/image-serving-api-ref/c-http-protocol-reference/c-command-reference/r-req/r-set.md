---
description: Information om medieuppsättning.
solution: Experience Manager
title: set
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# set{#set}

Information om medieuppsättning.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">-kodning</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Unik identifierare för begäran </p></td> 
 </tr> 
</table>

Returnerar information om bilder, videoklipp, färgrutor och olika metadata som är associerade med katalogen::ImageSet för bildkatalogposten som anges i URL-sökvägen. Det här svaret är en hierarkisk struktur som bestäms av typen av uppsättning. Lämplig formatering används när formatet &#39;xml&#39; eller &#39;json&#39; begärs.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::NonImgExpiration`.

>[!NOTE]
>
>Kolontecknet tillåts inte i req=set-begäranden.

Begäranden som stöder JSON-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
