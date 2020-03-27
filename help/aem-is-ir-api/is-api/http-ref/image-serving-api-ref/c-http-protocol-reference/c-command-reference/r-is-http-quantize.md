---
description: Färgkvantifiering. Anger färgkvantifieringsattribut för GIF-utdatakonvertering.
seo-description: Färgkvantifiering. Anger färgkvantifieringsattribut för GIF-utdatakonvertering.
seo-title: kvantifiera
solution: Experience Manager
title: kvantifiera
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# kvantifiera{#quantize}

Färgkvantifiering. Anger färgkvantifieringsattribut för GIF-utdatakonvertering.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> text </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Anger paletttyp. </p> <p>Ange till <span class="codeph"> adaptiv </span> för att beräkna en optimal palett för bilden. </p> <p>Välj en fördefinierad palett genom att välja <span class="codeph"> web </span> eller <span class="codeph"> mac </span> . </p> <p> <p>Obs!  Den <span class="codeph"> mac- </span> lastpallstypen stöds bara för GIF- och PNG8-format, men inte för formaten GIF-Alpha och PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gitter </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>Anger gitteralternativ. </p> <p>Ange som <span class="codeph"> diffusion </span> för felspridning i Floyd-Steinberg </p> <p>Inaktivera <span class="codeph"> gitter </span> om du vill inaktivera gitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span></span> </p> </td> 
   <td colname="col2"> <p>Antal utdatafärger (2-256) </p> <p>Anger hur många färger som ska ingå i den <span class="codeph"> adaptiva </span> paletten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span></span> </p> </td> 
   <td colname="col2"> <p>En kommaavgränsad lista med tvingade RGB-färger i hex6-format </p> <p>Här kan du ange färger som ska ingå i en <span class="codeph"> adaptiv </span> palett. Om antalet angivna färger är mindre än <span class="codeph"> <span class="varname"> numColors </span> </span>beräknas ytterligare färger baserat på bildinnehållet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-8ab5035055b24b858270d260912a7f3d}

Begär attribut. Används oavsett aktuell lagerinställning. Används endast if `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`eller `fmt=png8-alpha`. I annat fall ignoreras.

Färgerna som anges med ` *`colorList`*` måste bestå av RGB-värden i hex6-format (se ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) utan prefixet `0x`. Inga andra färgspecifikationer tillåts. *`numColors`* måste vara mellan 2 och 256.

## Standard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Exempel {#section-e34aca7587d548a7ae9d4266b80c9451}

Generera en GIF-miniatyrbild med `web` paletten utan gitter:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Konvertera bilden till en GIF-bild med två toner och genomskinlighet och tvinga färger till svartvitt:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Se även {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
