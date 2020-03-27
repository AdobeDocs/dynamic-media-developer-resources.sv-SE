---
description: Information om medieuppsättning.
seo-description: Information om medieuppsättning.
seo-title: set
solution: Experience Manager
title: set
topic: Scene7 Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# set{#set}

Information om medieuppsättning.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> kodning</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
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

Begäranden som stöder JSON-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för `req=` parametern:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
