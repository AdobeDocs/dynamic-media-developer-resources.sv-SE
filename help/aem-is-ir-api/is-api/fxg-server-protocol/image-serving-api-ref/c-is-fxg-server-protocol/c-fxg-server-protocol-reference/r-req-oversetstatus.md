---
description: Typ av begäran. Anger typen av begäran.
seo-description: Typ av begäran. Anger typen av begäran.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '249'
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
   <td colname="col2"> <p> Returnera en xml-lista med alla element med ett <span class="codeph"> s7:element</span>-attributvärde och en lista med alla sidor i fxg-dokumentet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Returnerar en XML-lista där <span class="codeph"> &lt;RichText/&gt;</span>-element är dolda. </p> <p>Returnerar en XML-lista med <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-element som är dolda för bearbetning på klientsidan. Endast <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-element som är dolda returneras. <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elementidis a required  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> attribute when using  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Alla dolda <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-element utan <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> visas inte. Varje <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-element i listan har <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> och begränsningsramen för den dolda textramen. Attributet <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> anger textindexet i artikeln som texten kunde få plats i ramen. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusonly gäller för  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> element i begärd FXG. Det listar inga <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>-element från inbäddade FXG:er. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> exists</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId unique request identifier </p> <p>Returnerar en enda egenskap med namnet catalogRecord.exists. Egenskapsvärdet anges till "1" om den angivna katalogposten finns i bilden eller standardkatalogen, och i annat fall är värdet "0". req=exists-begäranden mot kontexten /is/content anger om det finns en angiven post i den statiska innehållskatalogen eller inte. </p> </td> 
  </tr> 
 </tbody> 
</table>

