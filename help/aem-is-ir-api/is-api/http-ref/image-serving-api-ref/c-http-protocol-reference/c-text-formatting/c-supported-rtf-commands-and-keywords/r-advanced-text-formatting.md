---
description: Använd följande kommandon för avancerad textformatering.
solution: Experience Manager
title: Avancerad textformatering
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
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
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>Nedsänkt utan att teckensnittsstorleken ändras. </p> </td> 
   <td> <p>Position i halvpunkter; standard är 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>Upphöjd utan att teckensnittsstorleken ändras. </p> </td> 
   <td> <p>Position i halvpunkter; standard är 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>Inaktivera/aktivera vid angiven teckenstorlek. </p> </td> 
   <td> <p>Teckenstorleken i halvpunkter, över vilka kerning ska användas, 0 för att inaktivera kerning, standardvärdet är 1 för kerning av alla teckensnittsstorlekar över en halv punkt. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>Välj optisk kerning. </p> </td> 
   <td> <p> Endast <span class="codeph"> textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetrisk </span> </td> 
   <td> <p>Välj metrisk kerning. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expandera <span class="varname"> N </span> </span> </td> 
   <td> <p>Ändra teckenavstånd. </p> </td> 
   <td> <p>Positiva eller negativa kvartalspunkter. Standardvärdet är 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>Ändra teckenavstånd. </p> </td> 
   <td> <p>Positiva eller negativa twip. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Vågrät teckenskalning. </p> </td> 
   <td> <p>Positiv eller negativ procent. Standardvärdet är 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>Lodrät teckenskalning. </p> </td> 
   <td> <p>Positiv eller negativ procent, standardvärdet är 100, tillägget Dynamic Media. </p> <p> <span class="codeph"> \charscaley </span> skalförändrar även radavstånd när det används med <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> bevarar alltid radavstånd oavsett mängden lodrät teckenskalning. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Välj teckenflöde från vänster till höger. </p> </td> 
   <td> <p>Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Välj teckenflöde från höger till vänster. </p> </td> 
   <td> <p> Endast <span class="codeph"> text= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>Aktivera textpassning och ange största tillåtna teckenstorlek. </p> </td> 
   <td> <p>Teckensnittsstorlek i halvpunkter; <span class="codeph"> textPs= endast </span>; Dynamic Media-tillägg. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Maximal textpassning (mjuk begränsning). </p> </td> 
   <td> <p>0 utan radbegränsning; endast <span class="codeph"> textPs= </span>; Dynamic Media-tillägg. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Maximalt antal rader för textpassning (trunkering). </p> </td> 
   <td> <p> Endast <span class="codeph"> textPs= </span>; Dynamic Media-tillägg. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>Teckenorientering. </p> </td> 
   <td> <p> Endast <span class="codeph"> textPs= </span>; ignoreras för icke-romerska teckensnitt; ignoreras när <span class="codeph"> \stextflow1 </span> inte används. </p> <p>0 vertikalt (standard). </p> <p>1 roterad 90 grader medurs. </p> </td> 
  </tr> 
 </tbody> 
</table>
