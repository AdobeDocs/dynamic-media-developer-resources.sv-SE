---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primärFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Anger bildförstoringen för den utfällbara vyn i förhållande till huvudvyn. Måste vara ett heltal eller flyttal <span class="codeph"> 1.0</span> eller större. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Du kan ange en valfri sekundär faktor som du kan komma åt genom att klicka eller trycka på huvudvyn när högdagern är aktiv. Om du klickar eller trycker en andra gång återgår det till den primära zoomfaktorn. Värdet <span class="codeph"> -1</span> inaktiverar den sekundära zoomfaktorn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> uppskala</span></span> </p> </td> 
   <td colname="col2"> <p>Anger hur komponenten hanterar små bilder. </p> <p>Om det är inställt på <span class="codeph"> 1</span> skalar komponenten upp huvudbilden så att den passar i huvudvyn. Dessutom skalas zoombilden upp så att den fyller det utfällbara fönsterområdet. </p> <p>Om det är inställt på <span class="codeph"> 0</span> visas små bilder med den ursprungliga upplösningen och visas centrerat i huvudvisningsområdet och inuti det utfällbara fönstret. Du kan konfigurera extra tomt utrymme som visas runt bilden med en bakgrund eller liknande CSS-egenskap för CSS-klasserna <span class="codeph"> s7flyoutzoomview</span> och <span class="codeph"> s7flyoutzoom</span> i huvudvyn respektive det utfällbara fönstret. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
