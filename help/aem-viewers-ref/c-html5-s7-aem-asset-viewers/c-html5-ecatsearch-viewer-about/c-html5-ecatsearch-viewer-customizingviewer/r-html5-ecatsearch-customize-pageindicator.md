---
description: Sidindikatorn visar aktuellt sidindex och totalt sidantal. Den visas i huvudkontrollfältet på stationära datorer och surfplattor, och på mobiltelefoner läggs den till i sekundära kontrollfält. Sidindikatorn kan storleksanpassas, skalförändras och placeras med CSS.
seo-description: Sidindikatorn visar aktuellt sidindex och totalt sidantal. Den visas i huvudkontrollfältet på stationära datorer och surfplattor, och på mobiltelefoner läggs den till i sekundära kontrollfält. Sidindikatorn kan storleksanpassas, skalförändras och placeras med CSS.
seo-title: Sidindikator
solution: Experience Manager
title: Sidindikator
topic: Dynamic media
uuid: 1be6021b-3026-48ef-b121-eeb8270d2bae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sidindikator{#page-indicator}

Sidindikatorn visar aktuellt sidindex och totalt sidantal. Den visas i huvudkontrollfältet på stationära datorer och surfplattor, och på mobiltelefoner läggs den till i sekundära kontrollfält. Sidindikatorn kan storleksanpassas, skalförändras och placeras med CSS.

Indikatorn för utseendesidan styrs med följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Placera från huvudkontrollfältets övre kant (på stationära datorer och surfplattor) eller sekundära kontrollfält (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p>Placera från höger kant på huvudkontrollfältet (på stationära datorer och surfplattor) eller sekundärt kontrollfält (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster </span> </p> </td> 
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
   <td colname="col2"> <p>Teckensnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in en sidindikator som är 56 x 28 pixlar, vågrätt centrerad och placerad 4 pixlar från huvudkontrollfältets nederkant, och använda ett Helvetica-teckensnitt med 14 pixlar.

```
.s7ecatalogsearchviewer  .s7pageindicator { 
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

