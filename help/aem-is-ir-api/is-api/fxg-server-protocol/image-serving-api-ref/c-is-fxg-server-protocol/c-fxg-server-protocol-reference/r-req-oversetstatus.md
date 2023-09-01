---
title: req
description: Typ av begäran. Anger typen av begäran.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# req{#req}

Typ av begäran. Anger typen av begäran.

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Värde </th> 
   <th colname="col2" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> validera</span> </p> </td> 
   <td colname="col2"> <p> Returnerar eventuella fel vid återgivning av fxg med de angivna URL-modifierarna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> innehåll</span> </p> </td> 
   <td colname="col2"> <p> Returnera XML-lista med alla element med en <span class="codeph"> s7:element</span> attributvärde och en lista över alla sidor i fxg-dokumentet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Returnerar en XML-lista som <span class="codeph"> &lt;richtext /&gt;</span> -element är dolda. </p> <p>Returnerar en XML-lista med <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> element som är dolda för bearbetning på klientsidan. Endast <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> dolda element returneras. The <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> är obligatoriskt <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> attribut när de använder <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Valfri dold <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> element utan <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> finns inte med i listan. Varje <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -elementet i listan har <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>och markeringsramen för den dolda textramen. The <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> anger textindexet i artikeln till vilket texten passades in i ramen. The <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> gäller endast för <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -element i begärd FXG. Den listar inga <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> -element från inbäddade FXG-filer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> exists</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId unique request identifier </p> <p>Den returnerar en enda egenskap med namnet catalogRecord.exists. Egenskapsvärdet anges till "1" om den angivna katalogposten finns i bilden eller standardkatalogen, och i annat fall är värdet "0". req=exists-begäranden mot kontexten /is/content anger om det finns en angiven post i den statiska innehållskatalogen eller inte. </p> </td> 
  </tr> 
 </tbody> 
</table>
