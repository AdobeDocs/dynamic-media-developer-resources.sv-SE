---
description: Egenskaper för svarsdata. Utvärderar den aktuella begäran som om den vore en bildbegäran (req=img), men i stället för att returnera bilden returnerar servern de valda egenskaperna för svarsbilden.
solution: Experience Manager
title: proppar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# proppar{#props}

Egenskaper för svarsdata. Utvärderar den aktuella begäran som om den vore en bildbegäran (req=img), men i stället för att returnera bilden returnerar servern de valda egenskaperna för svarsbilden.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId </span> </span> </p> </td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p> </td> 
 </tr> 
</table>

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standard är `s7jsonResponse`.

Se [Egenskaper](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) för en beskrivning av svarssyntaxen och MIME-svarstypen. HTTP-svaret kan nås med en TTL som baseras på `attribute::NonImgExpiration`.

Följande egenskaper returneras för /is/image-begäranden:

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> Egenskap</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> Beskrivning</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> Bakgrundsfärg (se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p> heltal </p> </td> 
   <td> <p> Svarets bildhöjd i pixlar </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> boolesk </p> </td> 
   <td> <p> True if the ICC profile is embedded in the reply image. (Se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Namn/beskrivning av profilen som är associerad med svarsbilden. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> heltal </p> </td> 
   <td> <p> Svarsstorlek i pixlar som inte innehåller HTTP-huvudet; 0 om data från svarsbilden inte har cachelagrats tidigare av servern. (Se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadCache </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 1 om svarsbilden innehåller en alfakanal, annars 0. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Svarsbildtyp, kan vara <span class="codeph"> CMYK </span>, <span class="codeph"> RGB </span> eller <span class="codeph"> BW </span> (för gråskalebilder). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> boolesk </p> </td> 
   <td> <p> 1 om svarsbilden bäddar in banor, annars 0. (Se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> Utskriftsupplösning (dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p> heltal </p> </td> 
   <td> <p> JPEG-kvalitet. (Se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Mime-typ för svarsbilden. (Se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> heltal </p> </td> 
   <td> <p> Svarsbildens bredd i pixlar. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> boolesk </p> </td> 
   <td> <p> 1 om svarsbilden bäddar in xmp-data, annars 0. (Se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Identifierare för bildversion. (Se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Versionsidentifierare för metadata. (Se <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

Följande egenskaper returneras för `/is/content` begäranden:

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> Egenskap</b> </td> 
   <td> <b> Typ</b> </td> 
   <td> <b> Beskrivning</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> bana </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Delvis löst filsökväg. (Se <span class="codeph"> static::Path </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Objektfilens storlek i byte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> förfallodatum </span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> static::Expiration </span> eller standardtiden för live </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Datum/tid för ändring (från <span class="codeph"> static::TimeStamp </span> eller objektfilen) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> static::UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
