---
description: Du kan använda Image Serving för att hantera innehåll som inte är en bild i kataloger och hantera det via en separat /is/content-kontext.
seo-description: Du kan använda Image Serving för att hantera innehåll som inte är en bild i kataloger och hantera det via en separat /is/content-kontext.
seo-title: Hantera statiskt innehåll (inte bildinnehåll)
solution: Experience Manager
title: Hantera statiskt innehåll (inte bildinnehåll)
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Hantera statiskt innehåll (inte bildinnehåll){#serving-static-non-image-contents}

Du kan använda Image Serving för att hantera innehåll som inte är en bild i kataloger och hantera det via en separat /is/content-kontext.

Med den här funktionen kan du konfigurera TTL-värdet för varje objekt separat.

Image Serving har stöd för följande kommandon på [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Innehållstypfilter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>och <span class="codeph"> req=exists </span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache </a> </p> </td> 
  <td class="stentry"> <p>Tillåter att cachelagring på klientsidan inaktiveras. </p> </td> 
 </tr> 
</table>

## Grundläggande syntax {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> förfrågan </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> item </span>][? <span class="varname"> modifierare </span>] </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> katalog </span></span> </p> </td> 
  <td class="stentry"> <p>Katalogidentifierare. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> artikel </span></span> </p> </td> 
  <td class="stentry"> <p>Statiskt innehållsobjekt-ID. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modifierare </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span>*[&amp; <span class="varname"> command </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kommando </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> värde </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span></span> </p> </td> 
  <td class="stentry"> <p>Ett av de kommandonamn som stöds. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> värde </span></span> </p> </td> 
  <td class="stentry"> <p>Kommandovärde. </p> </td> 
 </tr> 
</table>

## Kataloger med statiskt innehåll {#section-91014f17f0d543d7aaf24539b2d7d4b9}

Kataloger med statiskt innehåll liknar bildkataloger, men har stöd för färre datafält:

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut/data </p> </th> 
   <th colname="col2" class="entry"> <p>Anteckningar </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::ID </span> </p> </td> 
   <td colname="col2"> <p>Katalogens post-ID för det här statiska innehållsobjektet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::Path </span> </p> </td> 
   <td colname="col2"> <p>Filsökvägen för det här innehållsobjektet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::Förfallotid </span> </p> </td> 
   <td colname="col2"> <p>TTL för detta innehållsobjekt; <span class="codeph"> attribute::Expiration </span> används om den inte anges eller om den är tom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>Tidsstämpel för ändring av fil. krävs när katalogbaserad validering har aktiverats med <span class="codeph"> attributet::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>Valfria metadata som är kopplade till detta statiska innehållsobjekt. tillgänglig för klienten med <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Valfri datatyp. kan användas för att filtrera begäranden om statiskt innehåll med kommandot <span class="codeph"> type= </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrera statiskt innehåll {#section-4c41bf41ff994910840c1352683d1f37}

Den här mekanismen kan hjälpa till att säkerställa att klienter endast får det innehåll som passar deras behov. Om det statiska innehållet är taggat med rätt `catalog::UserType` värden kan klienten lägga till `type=` kommandot i begäran. Bildservning jämför värdet som anges med `type=` kommandot med värdet för `catalog::UserType` och returnerar ett fel i stället för eventuellt olämpligt innehåll om det inte matchar.

## Bildtextfiler för video {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Du kan kapsla in videobeskrivningsfiler (WebVTT), CSS eller valfri textfil i JSONP-format. JSON-svaret beskrivs nedan.

* För WebVTT-filer är MIME-typen för svaret text/javascript. JSON returneras inte. I stället returneras Javascript som anropar en metod med JSON. Både ID och hanterare är valfria.
* För CSS-filer är MIME-typen för svaret text/javascript. Både ID och hanterare är valfria.
* Som standard används UTF-8-kodning för att säkerställa att den avkodas korrekt. Standardstorleksgränsen är 2 MB.

Du kan också använda spår för andra typer av tidsbestämda metadata. Källdata för varje spårelement är en textfil som består av en lista med tidsbestämda tips. Cues kan innehålla data i format som JSON eller CSV.

Mer information om JSONP-formatet finns i [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) .

Mer information om JSON-formatet finns i [www.json.org](http://www.json.org) .

## Se även {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Image Catalog Reference](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
