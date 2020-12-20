---
description: Begär validering.
seo-description: Begär validering.
seo-title: validera
solution: Experience Manager
title: validera
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# validera{#validate}

Begär validering.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

Tolkar begärandesträngen som om `req=img` hade angetts, men utan att variablerna ersätts och refererade objekt utvärderas (bilder, ICC-profiler, teckensnitt o.s.v.). Standardfelsvaret returneras om tolkningen misslyckas, annars returneras följande egenskap:

`request.isValid=1`

HTTP-svaret är inte tillgängligt.

Begäranden som stöder JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.
