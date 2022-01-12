---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primärFactor`*[,[ *`secondaryFactor`*][, *`uppskala`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primärFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Anger bildförstoringen för den utfällbara vyn i förhållande till huvudvyn. Måste vara ett heltal eller flyttal <span class="codeph"> 1.0</span> eller större. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Du kan ange en valfri sekundär faktor som du kan komma åt genom att klicka eller trycka på huvudvyn när högdagern är aktiv. Om du klickar eller trycker en andra gång återgår det till den primära zoomfaktorn. Värdet för <span class="codeph"> -1</span> inaktiverar den sekundära zoomfaktorn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> uppskala</span></span> </p> </td> 
   <td colname="col2"> <p>Anger hur komponenten hanterar små bilder. </p> <p>Om inställt på <span class="codeph"> 1</span> komponenten skalar upp huvudbilden så att den passar i huvudvyn. Dessutom skalas zoombilden upp så att den fyller det utfällbara fönsterområdet. </p> <p>Om inställt på <span class="codeph"> 0</span>små bilder visas med den ursprungliga upplösningen och centrerade i huvudvisningsområdet och inuti det utfällbara fönstret. Du kan konfigurera extra tomt utrymme som visas runt bilden med en bakgrund eller liknande CSS-egenskap för <span class="codeph"> s7flyoutzoomview</span> och <span class="codeph"> s7flyoutzoom</span> CSS-klasser i huvudvyn respektive det utfällbara fönstret. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
