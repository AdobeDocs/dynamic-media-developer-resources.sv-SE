---
description: Följande dokumentegenskaper stöds i textrutor.
seo-description: Följande dokumentegenskaper stöds i textrutor.
seo-title: Dokumentegenskaper (textruta)
solution: Experience Manager
title: Dokumentegenskaper (textruta)
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 743a773a-83b0-4667-9c67-4cefbfe77bbd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Dokumentegenskaper (textruta){#document-text-box-properties}

Följande dokumentegenskaper stöds i textrutor.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Kommando</b> </th> 
   <th class="entry"> <b>Beskrivning</b> </th> 
   <th class="entry"> <b>Anteckningar</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl  </span> </td> 
   <td> <p>Teckensnittstabell. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Teckenuppsättning för teckensnittet <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>RGB-färgtabell. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>CMYK-färgtabell. </p> </td> 
   <td> <p>Dynamic Media-tillägg. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>Färgtabell för bildservningsfärger. </p> </td> 
   <td> <p>Dynamic Media-tillägg; Endast <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Röd färgkomponent. </p> </td> 
   <td> <p>Får endast förekomma i <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Grön färgkomponent. </p> </td> 
   <td> <p>Får endast förekomma i <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Blå färgkomponent. </p> </td> 
   <td> <p>Får endast förekomma i <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Cyanfärgskomponent. </p> </td> 
   <td> <p>Dynamic Media-tillägg; får endast förekomma i <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Magentafärgkomponent. </p> </td> 
   <td> <p>Dynamic Media-tillägg; får endast förekomma i <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Gul färgkomponent. </p> </td> 
   <td> <p>Dynamic Media-tillägg; får endast förekomma i <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Svart färgkomponent. </p> </td> 
   <td> <p>Dynamic Media-tillägg; får endast förekomma i <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Vänstermarginal. </p> </td> 
   <td> <p>Virvlar; Endast <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Högermarginal. </p> </td> 
   <td> <p>Virvlar; Endast <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Övre marginal. </p> </td> 
   <td> <p>Virvlar; Endast <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Undre marginal. </p> </td> 
   <td> <p>Virvlar; Endast <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>Justera text uppåt i textrutan. </p> </td> 
   <td> <p>Standard </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>Justera text nedåt i textrutan. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>Centrera text i textruta. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Textflödesorientering. </p> </td> 
   <td> <p>Språkspecifikt textflöde. <span class="codeph"> textPs= </span> endast 0 (standard) vänster-höger, top-bottom (europeisk) 1 top-bottom, right-left (far Eastern) </p> </td> 
  </tr> 
 </tbody> 
</table>

