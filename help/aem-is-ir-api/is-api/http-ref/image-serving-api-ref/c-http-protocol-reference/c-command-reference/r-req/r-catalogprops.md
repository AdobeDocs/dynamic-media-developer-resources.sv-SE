---
description: Egenskaper för bildkatalog. Returnerar gemensamma attribut för den bildkatalog som anges i sökvägen för begäran.
solution: Experience Manager
title: katalogprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# katalogprops{#catalogprops}

Egenskaper för bildkatalog. Returnerar gemensamma attribut för den bildkatalog som anges i sökvägen för begäran.

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Unik identifierare för begäran. </p></td> 
 </tr> 
</table>

Om du vill hämta standardkatalogegenskaperna ( [!DNL default.ini]) utelämnar du katalog-ID:t. HTTP-svaret kan nås med TTL-värdet baserat på `attribute::NonImgExpiration`.

Begäranden som har stöd för JSONP-svarsformatet gör att du kan ange namnet på JS-callback-hanteraren med den utökade syntaxen för parametern `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` är namnet på JS-hanteraren som finns i JSONP-svaret. Endast tecknen a-z, A-Z och 0-9 tillåts. Valfritt. Standardvärdet är `s7jsonResponse`.

Följande egenskapsvärden returneras:

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> egenskap </b> </td> 
   <td> <b> Typ </b> </td> 
   <td> <b> Motsvarande katalogattribut </b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> <span class="codeph">-attribut::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-katalog::defaultExt</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph">-attribut::DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph">-attribut::DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix </span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph">-attribut::DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.expiration</span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> <span class="codeph">-attribut::Förfallotid</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> <span class="codeph">-attribut::DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration </span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> <span class="codeph">-attribut::NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph">-attribut::LastModified</span>, eller, om det inte finns, den senaste ändringstiden för <span class="varname">-katalogfilen </span><span class="filepath"> .ini</span>-filen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> <span class="codeph">-attribut::JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph">-attribut::MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph">-attribut::PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph">-attribut::PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph">-attribut::ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> <span class="codeph">-attribut::Upplösning</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor </span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> <span class="codeph">-attribut::ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph">-attribut::ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> verklig </p> </td> 
   <td> <p> <span class="codeph">-attribut::ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph">-attribut::ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph">-attribut::ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::watermark</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph">-attribut::Vattenstämpel</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
