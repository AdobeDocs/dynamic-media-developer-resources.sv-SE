---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> markera|markör  </span> </p> </td> 
   <td colname="col2"> <p> Anger vilken typ av navigeringsram som ska användas. När komponenten är inställd på <span class="codeph"> markör </span> använder den en referensmarkör med fast storlek. Det går att ha olika markörgrafik för datorer och pekenheter. Den styrs med <span class="codeph"> .s7cursor </span> CSS-klassen och <span class="codeph"> input=mouse|touch </span>-attributväljaren. På stationära datorer ställs en fästpunkt in mitt i markörområdet, medan fästpunkten finns längst ned i mitten av markören på pekenheter. När komponenten är inställd på <span class="codeph"> markera </span> används en navigeringsram i variabel storlek; ramens storlek och form beror på zoomfaktorn och den utfällbara vyns storlek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger den tid (i sekunder) det tar för markören att tonas in efter att den har aktiverats av användaren. Tona in används endast på pekenheter. på datorsystem ignoreras det av komponenten. </p> <p>Tona in gäller för följande gränssnittselement: markera bildruta, fast markör, övertäckning (i fallet <span class="codeph"> är övertäckningsparametern </span> inställd på <span class="codeph"> 1 </span>). Animeringen i den utfällbara vyn börjar först när markeringen/markören har tonats in i animeringen. Det finns ingen tonad animering. När användaren inaktiverar den utfällbara menyn döljs motsvarande gränssnittselement (markör, högdager och övertäckning) omedelbart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> Styr placeringen av navigeringsramen. </p> <p>Om du anger <span class="codeph"> på bild </span> kan navigeringsramen bara placeras inuti det faktiska bildområdet i huvudvyn. </p> <p>Om den är inställd på <span class="codeph"> free </span> kan användaren flytta navigeringsramen vart som helst i det logiska huvudvisningsområdet, även utanför bildinnehållet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
