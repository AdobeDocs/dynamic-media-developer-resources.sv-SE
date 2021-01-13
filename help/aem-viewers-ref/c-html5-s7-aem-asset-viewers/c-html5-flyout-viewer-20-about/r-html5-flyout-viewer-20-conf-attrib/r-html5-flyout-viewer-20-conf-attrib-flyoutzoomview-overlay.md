---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Styr högdagerutseendet för huvudvyn när den utfällbara menyn är aktiv. När det är inställt på <span class="codeph"> 0</span> markeras det område som är synligt i det utfällbara fönstret med format som finns i antingen <span class="codeph"> .s7highlight</span> eller <span class="codeph"> .s7cursor</span> CSS-klassnamn (beroende på värdet för <span class="codeph"> highlightmode</span> modifierare). Om <span class="codeph"> 1</span>-komponenten anges som  aktiveras inverterat läge där det område som visas för närvarande antingen är helt genomskinligt (om <span class="codeph"> markeringsläge</span> är inställt på <span class="codeph"> markera</span>) eller formaterat med <span class="codeph"> .s7cursor</span> CSS-klassnamn (i <span class="codeph"> markeringsläge</span> är inställt på <span class="codeph">-markören</span>), men det omgivande området fylls med format som tillhandahålls av <span class="codeph"> .s7overlay</span> CSS-klassnamn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
