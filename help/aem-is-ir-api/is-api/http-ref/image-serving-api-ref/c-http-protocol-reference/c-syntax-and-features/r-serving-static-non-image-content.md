---
description: Serverar statiskt (icke-bildinnehåll) innehåll
solution: Experience Manager
title: Serverar statiskt (icke-bildinnehåll) innehåll
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Serverar statiskt (icke-bildinnehåll) innehåll{#serving-static-non-image-content}

Image Serving är ett sätt att hantera innehåll som inte finns i bilder i kataloger och hantera det via en separat `context /is/content`. Mekanismen gör det möjligt att konfigurera TTL för varje objekt separat.

## Grundläggande syntax {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> förfrågan </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> server </span>/is/content[/ <span class="varname"> katalog </span>/ <span class="varname"> artikel </span>][? <span class="varname"> modifierare </span>] </span> </p> </td> 
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

## Kommandoöversikt {#section-61657a0141914053ab12038ad7e91500}

Image Serving stöder följande kommandon på /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>Innehållstypfilter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>och <span class="codeph"> req=exists </span> endast. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache </a> </td> 
  <td class="stentry"> <p>Tillåter att cachelagring på klientsidan inaktiveras. </p> </td> 
 </tr> 
</table>

## Kataloger med statiskt innehåll {#section-b2b8f4860fe84e528493ed704c7c5141}

Kataloger med statiskt innehåll liknar bildkataloger, men har stöd för färre datafält:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/data</b> </th> 
   <th class="entry"> <b> Anteckningar</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::ID </span> </p> </td> 
   <td> <p> Katalogens post-ID för det här statiska innehållsobjektet </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::Path </span> </p> </td> 
   <td> <p> Filsökvägen för det här innehållsobjektet </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::Förfallotid </span> </p> </td> 
   <td> <p> TTL för det här innehållsobjektet; attribute::Expiration används om inget anges eller om det är tomt </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::TimeStamp </span> </p> </td> 
   <td> <p> Tidsstämpel för filändring; krävs när katalogbaserad validering har aktiverats med attributet::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::UserData </span> </p> </td> 
   <td> <p> Valfria metadata associerade med det här statiska innehållsobjektet, tillgängliga för klienten med req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> katalog::UserType </span> </p> </td> 
   <td> <p> Valfri datatyp; kan användas för att filtrera begäranden om statiskt innehåll med kommandot type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrera statiskt innehåll {#section-896c37cf68bc446eb0766fb378898262}

Den här mekanismen kan hjälpa till att säkerställa att klienter endast får det innehåll som passar deras behov. Anta att det statiska innehållet är taggat med lämpligt `catalog::UserType`värden kan klienten lägga till `type=` till begäran. Image Serving jämför värdet som anges med `type=` till värdet av `catalog::UserType` och returnera ett fel i stället för potentiellt olämpligt innehåll om det inte matchar.

## Se även {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Referens för bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
