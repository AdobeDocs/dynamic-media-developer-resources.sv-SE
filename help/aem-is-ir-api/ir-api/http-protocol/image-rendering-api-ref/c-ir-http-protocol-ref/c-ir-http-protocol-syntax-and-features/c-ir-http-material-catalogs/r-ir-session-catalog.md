---
description: Sessionskatalogen är den materialkatalog som innehåller sessionsattribut för begäran samt ett standard-catId-värde för alla kommandon src=, vignette= och icc=.
solution: Experience Manager
title: Sessionskatalog
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Sessionskatalog{#session-catalog}

Sessionskatalogen är den materialkatalog som innehåller sessionsattribut för begäran samt ett standard-catId-värde för alla kommandon src=, vignette= och icc=.

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
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> Rotsökväg för materialdatafiler </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::VignettePath</span> </p> </td> 
   <td> <p> Rotsökväg för vinjettfiler </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::IccProfileRgb</span> </p> </td> 
   <td> <p> Standardarbetsfärgrymd om en vinjettering inte bäddar in en ICC-profil </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> Rot-URL för relativa HTTP-filsökvägar i <span class="codeph"> src=</span>-kommandon </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Inledande läge för att visa/dölja för överlappande objekt </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> Svarsbildens TTL-värde (Time-to-live) för proxyservern och webbläsarcachen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> Högsta tillåtna svarsbildens bredd och höjd </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> Standardvärden för <span class="codeph"> wid=</span> och <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> Standardvärde för <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> Standardvärde för <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> Komprimeringstyp för TIFF-bildutdata </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Sharpen</span> </p> </td> 
   <td> <p> Standardvärde för <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> Anger beteende när ett <span class="codeph"> sel=</span>-kommando misslyckas </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> Anger beteende när ett <span class="codeph"> obj=</span>-kommando misslyckas </p> </td> 
  </tr> 
 </tbody> 
</table>
