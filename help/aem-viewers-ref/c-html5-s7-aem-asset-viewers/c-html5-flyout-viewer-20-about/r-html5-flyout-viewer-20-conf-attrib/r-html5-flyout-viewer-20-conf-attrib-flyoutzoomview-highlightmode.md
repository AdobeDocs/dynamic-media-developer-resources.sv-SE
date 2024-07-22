---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> markering|markör </span> </p> </td> 
   <td colname="col2"> <p> Anger vilken typ av navigeringsram som ska användas. När komponenten är inställd på <span class="codeph"> cursor </span> använder den en referensmarkör med fast storlek. Det går att ha olika markörgrafik för datorer och pekenheter. Den här funktionen styrs med CSS-klassen <span class="codeph"> .s7cursor </span> och attributväljaren <span class="codeph"> input=mouse|touch </span> . På stationära datorer ställs en fästpunkt in mitt i markörområdet, medan fästpunkten finns längst ned i mitten av markören på pekenheter. När komponenten är inställd på <span class="codeph"> markering </span> använder den en navigeringsram med variabel storlek. Bildrutans storlek och form beror på zoomfaktorn och storleken på den utfällbara vyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger den tid (i sekunder) det tar för markören att tonas in efter att den har aktiverats av användaren. Tona in används bara på pekenheter. På skrivbordssystem ignoreras det av komponenten. </p> <p>Tona in gäller för följande gränssnittselement: markeringsram, fast markör, övertäckning (om parametern <span class="codeph"> overlay </span> är inställd på <span class="codeph"> 1 </span>). Animeringen i den utfällbara vyn börjar först när markeringen/markören har tonats in i animeringen. Det finns ingen uttonad animering. När användaren inaktiverar den utfällbara menyn döljs motsvarande gränssnittselement (markör, högdager och övertäckning) omedelbart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Styr placeringen av navigeringsramen. </p> <p>Om värdet är <span class="codeph"> onimage </span> kan navigeringsramen bara placeras inuti det faktiska bildområdet i huvudvyn. </p> <p>Om värdet är <span class="codeph"> free </span> kan användaren flytta navigeringsramen vart som helst i det logiska huvudvisningsområdet, även utanför bildinnehållet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
