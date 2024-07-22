---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Styr högdagerutseendet för huvudvyn när den utfällbara menyn är aktiv. När värdet är <span class="codeph"> 0</span> markeras det område som är synligt i det utfällbara fönstret med format från <span class="codeph"> .s7highlight</span> eller från <span class="codeph"> .s7cursor</span> CSS-klassnamn (beroende på värdet för <span class="codeph"> highlightmode </span> -modifierare). När <span class="codeph"> 1</span> -komponenten ställs in på inverterat läge där det visningsområde som visas antingen är helt genomskinligt (om <span class="codeph"> highlightmode </span> är inställt på <span class="codeph"> highlight</span>) eller formaterat med <span class="codeph"> .s7cursor</span> CSS-klassnamn (om <span class="codeph"> highlightmode </span> är inställt på <span class="codeph"> cursor </span>), men det omgivande området fylls med format från CSS-klassnamnet <span class="codeph"> .s7overlay </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
