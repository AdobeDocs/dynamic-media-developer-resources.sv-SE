---
description: Färgkvantifiering. Anger färgkvantifieringsattribut för GIF-utdatakonvertering.
solution: Experience Manager
title: kvantifiera
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# kvantifiera{#quantize}

Färgkvantifiering. Anger färgkvantifieringsattribut för GIF-utdatakonvertering.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}  </span> palettyp </p> <p>Välj <span class="codeph"> web </span> eller <span class="codeph"> mac </span> om du vill välja en fördefinierad palett, eller ange <span class="codeph"> adaptive </span> om du vill beräkna en optimal palett för bilden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> gitter  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off}  </span> gitteralternativ </p> <p>Välj 'diffuse' för Floyd-Steinberg-feldiffusion eller 'off' för att inaktivera gitter. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Antal utdatafärger (heltal) som ingår i paletten <span class="codeph"> adaptiv </span>. </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> måste vara mellan 2 och 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Kommaavgränsad lista med tvingade RGB-färger i hex6-format. Gör att du kan ange tvingade färger som ska inkluderas i en <span class="codeph"> adaptiv </span>-palett. Om antalet angivna färger är mindre än <span class="codeph"> numColors </span> beräknas ytterligare färger baserat på bildinnehållet. </p> <p>Används endast om <span class="codeph"> fmt=gif </span> eller <span class="codeph"> fmt=gif-alpha </span>. I annat fall ignoreras. Färgerna som anges med <span class="codeph"> <span class="varname"> colorList </span> </span> måste vara RGB-värden i hex6-format (se <span class="codeph"> color </span>); inga andra färgspecifikationer tillåts. </p> </td> 
 </tr> 
</table>

## Standard {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exempel {#section-b3a979dc9ae3459baa093bf17310988f}

Generera en GIF-miniatyrbild med paletten `web` utan gitter:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Konvertera bilden till en GIF-bild med två toner och genomskinlighet och tvinga färger till svartvitt:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
