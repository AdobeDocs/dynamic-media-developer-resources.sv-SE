---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primärFactor</span></span> </p> </td> 
   <td colname="col2"> <p> Anger bildförstoringen för den utfällbara vyn i förhållande till huvudvyn. Måste vara ett heltal eller flyttal <span class="codeph"> 1,0</span> eller större. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> SecondaryFactor</span></span> </p> </td> 
   <td colname="col2"> <p> Du kan ange en valfri sekundär faktor som du kan komma åt genom att klicka eller trycka på huvudvyn när högdagern är aktiv. Om du klickar eller trycker en andra gång återgår det till den primära zoomfaktorn. Värdet <span class="codeph"> -1</span> inaktiverar den sekundära zoomfaktorn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> uppskala</span></span> </p> </td> 
   <td colname="col2"> <p>Anger hur komponenten hanterar små bilder. </p> <p>Om den är inställd på <span class="codeph"> 1</span> skalas huvudbilden upp så att den passar i huvudvyn. Dessutom skalas zoombilden upp så att den fyller det utfällbara fönsterområdet. </p> <p>Om värdet är <span class="codeph"> 0</span> visas små bilder med den ursprungliga upplösningen och centrerade i huvudvisningsområdet och inuti det utfällbara fönstret. Du kan konfigurera extra tomt utrymme som visas runt bilden med en bakgrund eller liknande CSS-egenskap i CSS-klasserna <span class="codeph"> s7flyoutzoomview</span> och <span class="codeph"> s7flyoutzoom</span> i huvudvyn respektive det utfällbara fönstret. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
