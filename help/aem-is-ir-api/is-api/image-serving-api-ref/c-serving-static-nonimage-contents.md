---
title: Hantera statiskt innehåll (inte bildinnehåll)
description: Du kan använda Image Serving för att hantera innehåll som inte är en bild i kataloger och hantera det via en separat /is/content-kontext.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Hantera statiskt innehåll (inte bildinnehåll){#serving-static-non-image-contents}

Du kan använda Image Serving för att hantera innehåll som inte är en bild i kataloger och hantera det via en separat /is/content-kontext.

Med den här funktionen kan du konfigurera TTL-värdet för varje objekt separat.

Image Serving stöder följande kommandon på [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Innehållstypfilter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>och <span class="codeph"> req=exists </span> endast. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache </a> </p> </td> 
  <td class="stentry"> <p>Tillåter att cachelagring på klientsidan inaktiveras. </p> </td> 
 </tr> 
</table>

## Grundläggande syntax {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> förfrågan </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> artikel </span>][? <span class="varname"> modifierare </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> katalog </span> </span> </p> </td> 
  <td class="stentry"> <p>Katalogidentifierare. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> artikel </span> </span> </p> </td> 
  <td class="stentry"> <p>Statiskt innehållsobjekt-ID. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modifierare </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kommando </span>*[&amp; <span class="varname"> kommando </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kommando </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>Ett av de kommandonamn som stöds. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
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
   <td colname="col2"> <p>TTL för detta innehållsobjekt; <span class="codeph"> attribute::Expiration </span> används om inget anges eller om det är tomt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>Tidsstämpel för ändring av fil. krävs när katalogbaserad validering är aktiverad med <span class="codeph"> attribute::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>Valfria metadata som är kopplade till detta statiska innehållsobjekt. som är tillgängliga för klienten med <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> katalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Valfri datatyp. kan användas för att filtrera begäranden om statiskt innehåll med <span class="codeph"> type=, kommando </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrera statiskt innehåll {#section-4c41bf41ff994910840c1352683d1f37}

Den här mekanismen kan hjälpa till att säkerställa att klienter endast får det innehåll som passar deras behov. Anta att det statiska innehållet är taggat med lämpligt `catalog::UserType` värden kan klienten lägga till `type=` till begäran. Image Serving jämför värdet som anges med `type=` till värdet av `catalog::UserType` och om det finns en avvikelse returneras ett fel i stället för potentiellt olämpligt innehåll.

## Bildtextfiler för video {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Du kan kapsla in videobeskrivningsfiler (WebVTT), CSS eller valfri textfil i JSONP-format. JSON-svaret beskrivs nedan.

* För WebVTT-filer är MIME-typen för svaret text/javascript. JSON returneras inte. I stället returneras JavaScript som anropar en metod med JSON. Både ID och hanterare är valfria.
* För CSS-filer är MIME-typen för svaret text/javascript. Både ID och hanterare är valfria.
* Som standard används UTF-8-kodning för att säkerställa att den avkodas korrekt. Standardstorleksgränsen är 2 MB.

Du kan också använda spår för andra typer av tidsbestämda metadata. Källdata för varje spårelement är en textfil som består av en lista med tidsbestämda tips. Cues kan innehålla data i format som JSON eller CSV.

Se [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) om du vill ha mer information om JSONP-formatet.

Se [www.json.org](https://www.json.org/json-en.html) för mer information om JSON-formatet.

## Se även {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Referens för bildkatalog](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
