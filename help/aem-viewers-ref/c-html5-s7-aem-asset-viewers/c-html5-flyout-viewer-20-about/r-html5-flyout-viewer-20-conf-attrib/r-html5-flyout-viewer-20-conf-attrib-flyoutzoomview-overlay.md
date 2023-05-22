---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Styr högdagerutseendet för huvudvyn när den utfällbara menyn är aktiv. När inställt på <span class="codeph"> 0</span>markerar det område som visas i det utfällbara fönstret med hjälp av format från <span class="codeph"> .s7highlight</span> eller av <span class="codeph"> .s7cursor</span> CSS-klassnamn (beroende på värdet på <span class="codeph"> highlightmode</span> modifierare). När inställt på <span class="codeph"> 1</span> -komponenten försätts i "omvänd" läge där det för närvarande visade området antingen är helt genomskinligt (om det är <span class="codeph"> highlightmode</span> är inställd på <span class="codeph"> markera</span>) eller formaterad med <span class="codeph"> .s7cursor</span> CSS-klassnamn (om det är <span class="codeph"> highlightmode</span> är inställd på <span class="codeph"> markör</span>), men det omgivande området fylls med hjälp av format från <span class="codeph"> .s7overlay</span> CSS-klassnamn. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
