---
description: Använd följande kommandon för avancerad textformatering.
solution: Experience Manager
title: Avancerad textformatering
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Avancerad textformatering{#advanced-text-formatting}

Använd följande kommandon för avancerad textformatering.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Kommando </th> 
   <th class="entry"> Beskrivning </th> 
   <th class="entry"> Anteckningar </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Nedsänkt utan att teckensnittsstorleken ändras. </p> </td> 
   <td> <p>Positionera i halvpunkter. Standardvärdet är 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Upphöjd utan att teckensnittsstorleken ändras. </p> </td> 
   <td> <p>Positionera i halvpunkter. Standardvärdet är 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Inaktivera/aktivera vid angiven teckensnittsstorlek. </p> </td> 
   <td> <p>Teckenstorlek i halvpunkter över vilka kerning ska användas. 0 för att inaktivera kerning, Standardvärdet är 1 för kerning av alla teckensnittsstorlekar över en halv punkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical  </span> </td> 
   <td> <p>Välj optisk kerning. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetrisk  </span> </td> 
   <td> <p>Välj metrisk kerning. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \färdigställ  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Ändra teckenavstånd. </p> </td> 
   <td> <p>Positiva eller negativa kvartal. Standardvärdet är 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Ändra teckenavstånd. </p> </td> 
   <td> <p>Positiva eller negativa twip. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Vågrät teckenskalning. </p> </td> 
   <td> <p>Positiv eller negativ procent. Standardvärdet är 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Lodrät teckenskalning. </p> </td> 
   <td> <p>Positiv eller negativ procent. Standardvärdet är 100. Dynamic Media-tillägg. </p> <p> <span class="codeph"> \charscaley skaley skalar  </span> även radavstånd när det används med  <span class="codeph"> text=  </span>. <span class="codeph"> textPs= bevarar  </span> alltid radavstånd oavsett mängden lodrät teckenskalning. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>Välj teckenflöde från vänster till höger. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>Välj teckenflöde från höger till vänster. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Aktivera textpassning och ange största tillåtna teckenstorlek. </p> </td> 
   <td> <p>Teckenstorlek i halvpunkter; Endast <span class="codeph"> textPs= </span>; Dynamic Media-tillägg. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Maximal textpassning (mjuk begränsning). </p> </td> 
   <td> <p>0 utan linjebegränsning, Endast <span class="codeph"> textPs= </span>; Dynamic Media-tillägg. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Maximalt antal rader för textpassning (trunkering). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; Dynamic Media-tillägg. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Teckenorientering. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignoreras för icke-romerska teckensnitt, ignoreras när  <span class="codeph"> \stextflow1 inte  </span> används. </p> <p>0 vertikalt (standard). </p> <p>1 roterad 90 grader medurs. </p> </td> 
  </tr> 
 </tbody> 
</table>

