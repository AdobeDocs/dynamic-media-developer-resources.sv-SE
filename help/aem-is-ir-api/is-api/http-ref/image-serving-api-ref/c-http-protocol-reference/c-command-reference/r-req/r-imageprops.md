---
description: Source bildegenskaper. Returnerar markerade egenskaper för bildfilen eller katalogposten som anges i URL-sökvägen.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# imageprops{#imageprops}

Source bildegenskaper. Returnerar markerade egenskaper för bildfilen eller katalogposten som anges i URL-sökvägen.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

HTTP-svaret kan nås med TTL-värdet baserat på `attribute::NonImgExpiration`.

Andra kommandon i begärandesträngen ignoreras.

Begäranden som har stöd för JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.

Följande egenskaper returneras:

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> egenskap </b> </td> 
   <td> <b> Typ </b> </td> 
   <td> <b> Beskrivning</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph">-katalog::Ankarpunkt</span> eller standardfästpunkt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph">-katalog::Förfallotid</span> eller standardtid för direktuppspelning </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> heltal </p> </td> 
   <td> <p>Bildens höjd i pixlar med full upplösning </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Namn/beskrivning av profilen som är associerad med den här bilden </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-bild. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolesk </p> </td> 
   <td> <p> 1 om den associerade profilen är inbäddad i bilden </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> boolesk </p> </td> 
   <td> <p> 1 om bilden innehåller Photoshop sökvägsdata </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-bild. embeddedXmpData</span> </p> </td> 
   <td> <p> boolesk </p> </td> 
   <td> <p> 1 om bilden innehåller XMP data </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 för ingen mask, 1 för förmultiplicerad alfa, 2 för icke-förmultiplicerad alfa och 3 för en separat maskbild </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph">-katalog::Modifier</span> eller tom om det inte är en katalogpost </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-bild. photoshopPathNames</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Kommaavgränsad lista med namnen på alla Photoshop-sökvägar som är associerade med den här bilden </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Bildtypen kan vara CMYK, RGB eller BW (för gråskalebilder) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph">-attribut::PostModifier</span> eller tom om det inte är en katalogpost </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> standardutskriftsupplösning i pixlar/tum </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> <span class="codeph">-katalog::Upplösning</span> eller standardobjektets upplösning </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Ändringsdatum/tid (från <span class="codeph">-katalog::TimeStamp</span> eller bildfilen) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> <span class="codeph">-katalog::ThumbRes</span> eller standardupplösning för miniatyrbilder </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph">-katalog::ThumbType</span> eller standardminiatyrtyp </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> heltal </p> </td> 
   <td> <p> Bildbredd med full upplösning i pixlar </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translateId</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Katalog-ID som <span class="varname">-objektet </span> som anges i sökvägen tolkas till (se <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Översättning av objekt-ID </a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
