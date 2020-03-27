---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyoutTransition
solution: Experience Manager
title: FlyoutZoomView.flyoutTransition
topic: Dynamic media
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyoutTransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ingen|bild|tona </span></span> </p> </td> 
   <td colname="col2"> <p> Anger vilken typ av effekt som används när den utfällbara vyn visas eller döljs. Med <span class="codeph"> ingen </span>visas den utfällbara bilden omedelbart när den är aktiverad och klar. <span class="codeph"> bildrutan </span> får bildruteanimeringen att spelas upp från vänster till höger. Med <span class="codeph"> toning </span> används en alfablandning på den utfällbara bilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span></span> </p> </td> 
   <td colname="col2"> <p> Antal sekunder som det tar att slutföra animeringen av bildspelet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span></span> </p> </td> 
   <td colname="col2"> <p> Fördröjningen i sekunder mellan användaråtgärden som initierar visningsanimeringen och början av själva visningsanimeringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime </span></span> </p> </td> 
   <td colname="col2"> <p> Antal sekunder som det tar att slutföra animeringen som döljs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span></span> </p> </td> 
   <td colname="col2"> <p> Fördröjning i sekunder mellan användaråtgärd som initierar den dolda animeringen och början på själva animeringen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
