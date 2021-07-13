---
description: Färgkvantifiering. Anger färgkvantifieringsattribut för GIF-utdatakonvertering.
solution: Experience Manager
title: kvantifiera
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# kvantifiera{#quantize}

Färgkvantifiering. Anger färgkvantifieringsattribut för GIF-utdatakonvertering.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>Anger paletttyp. </p> <p>Ange <span class="codeph"> adaptiv </span> för att beräkna en optimal palett för bilden. </p> <p>Ange <span class="codeph"> web </span> eller <span class="codeph"> mac </span> om du vill välja en fördefinierad palett. </p> <p> <p>Obs!  Lastpallstypen <span class="codeph"> för mac </span> stöds bara för formaten GIF och PNG8, men inte för formaten GIF-Alpha och PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gitter  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off}  </span> </p> <p>Anger gitteralternativ. </p> <p>Ange <span class="codeph"> diffusion </span> för felspridning i Floyd-Steinberg </p> <p>Ange <span class="codeph"> av </span> om du vill inaktivera gitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>Antal utdatafärger (2-256) </p> <p>Anger hur många färger som ska ingå i paletten <span class="codeph"> adaptiv </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>En kommaavgränsad lista med tvingade RGB-färger i hex6-format </p> <p>Här kan du ange färger som ska ingå i en <span class="codeph"> adaptiv </span>-palett. Om antalet angivna färger är mindre än <span class="codeph"> <span class="varname"> numColors </span> </span> beräknas ytterligare färger baserat på bildinnehållet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-8ab5035055b24b858270d260912a7f3d}

Begär attribut. Används oavsett aktuell lagerinställning. Används endast om `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` eller `fmt=png8-alpha`. I annat fall ignoreras.

Färgerna som anges med `*`colorList`*` måste bestå av RGB-värden i hex6-format (se ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) utan prefixet `0x`. Inga andra färgspecifikationer tillåts. *`numColors`* måste vara mellan 2 och 256.

## Standard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Exempel {#section-e34aca7587d548a7ae9d4266b80c9451}

Generera en GIF-miniatyrbild med paletten `web` utan gitter:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Konvertera bilden till en GIF-bild med två toner och genomskinlighet och tvinga färger till svartvitt:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Se även {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [färg](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
