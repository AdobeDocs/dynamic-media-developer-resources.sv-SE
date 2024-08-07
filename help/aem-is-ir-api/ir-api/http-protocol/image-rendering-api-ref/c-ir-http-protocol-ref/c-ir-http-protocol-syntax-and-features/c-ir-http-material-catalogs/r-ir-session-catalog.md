---
title: Sessionskatalog
description: Sessionskatalogen är den materialkatalog som innehåller sessionsattribut för begäran och ett standard-catId-värde för alla kommandon src=, vignette= och icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Sessionskatalog{#session-catalog}

Sessionskatalogen är den materialkatalog som innehåller sessionsattribut för begäran och ett standard-catId-värde för alla `src=`-, `vignette=`- och `icc=`-kommandon.

Sessionskatalogen anges som det första sökvägselementet i sökvägen för HTTP-begäran (omedelbart efter servernamnet). Om det första sökvägselementet inte matchar attributet::RootId för någon katalog används standardkatalogen som sessionskatalog.

Sessionskatalogen innehåller följande standardvärden för sessioner:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Anteckningar </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::RootPath</span> </p> </td> 
   <td> <p> Rotsökväg för materialdatafiler </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::VignettePath</span> </p> </td> 
   <td> <p> Rotsökväg för vinjettfiler </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::IccProfileRgb</span> </p> </td> 
   <td> <p> Standardarbetsfärgrymd om en vinjettering inte bäddar in en ICC-profil </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::RootUrl</span> </p> </td> 
   <td> <p> Rot-URL för relativa HTTP-filsökvägar i kommandona <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Inledande läge för att visa/dölja för överlappande objekt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::Förfallotid</span> </p> </td> 
   <td> <p> Svarsbildens TTL-värde (Time-to-live) för proxyservern och webbläsarcachen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::MaxPix</span> </p> </td> 
   <td> <p> Högsta tillåtna svarsbildens bredd och höjd </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::DefaultPix</span> </p> </td> 
   <td> <p> Standardvärden för <span class="codeph"> wid=</span> och <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::Format</span> </p> </td> 
   <td> <p> Standardvärde för <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::JpegQuality</span> </p> </td> 
   <td> <p> Standardvärde för <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::TiffEncoding</span> </p> </td> 
   <td> <p> Komprimeringstyp för TIFF-bildutdata </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::Skärpa</span> </p> </td> 
   <td> <p> Standardvärde för <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::OnFailSel</span> </p> </td> 
   <td> <p> Anger beteende när ett <span class="codeph"> sel=</span>-kommando misslyckas </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-attribut::OnFailObj</span> </p> </td> 
   <td> <p> Anger beteende när ett <span class="codeph"> obj=</span>-kommando misslyckas </p> </td> 
  </tr> 
 </tbody> 
</table>
