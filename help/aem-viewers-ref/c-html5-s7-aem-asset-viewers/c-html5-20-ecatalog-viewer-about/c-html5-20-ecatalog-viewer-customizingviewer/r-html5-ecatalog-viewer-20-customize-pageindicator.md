---
title: Sidindikator
description: Sidindikatorn visar aktuellt sidindex och totalt sidantal. Den visas i huvudkontrollfältet på stationära datorer och surfplattor, och på mobiltelefoner läggs den till i sekundära kontrollfält. Sidindikatorn kan storleksanpassas, skalförändras och placeras med CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c63af583-274c-4052-8186-604119a368af
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Sidindikator{#page-indicator}

Sidindikatorn visar aktuellt sidindex och totalt sidantal. Den visas i huvudkontrollfältet på stationära datorer och surfplattor, och på mobiltelefoner läggs den till i sekundära kontrollfält. Sidindikatorn kan storleksanpassas, skalförändras och placeras med CSS.

Utseendet på sidindikatorn styrs med följande CSS-klassväljare:

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> övre </span> </p> </td> 
   <td colname="col2"> <p>Placera från huvudkontrollfältets övre kant (på stationära datorer och surfplattor) eller sekundära kontrollfält (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p>Placera från höger kant på huvudkontrollfältet (på stationära datorer och surfplattor) eller sekundärt kontrollfält (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kvar </span> </p> </td> 
   <td colname="col2"> <p>Placera från vänster kant på huvudkontrollfältet (på stationära datorer och surfplattor) eller sekundärt kontrollfält (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p>Placera längst ned i huvudkontrollfältet (på stationära datorer och surfplattor) eller i det sekundära kontrollfältet (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Sidans bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Sidans höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Teckenfärg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Typsnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en sidindikator som är 56 x 28 pixlar, vågrätt centrerad och placerad 4 pixlar från huvudkontrollfältets nederkant, och använda ett Helvetica®-teckensnitt som är 14 pixlar.

```
.s7ecatalogviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```
