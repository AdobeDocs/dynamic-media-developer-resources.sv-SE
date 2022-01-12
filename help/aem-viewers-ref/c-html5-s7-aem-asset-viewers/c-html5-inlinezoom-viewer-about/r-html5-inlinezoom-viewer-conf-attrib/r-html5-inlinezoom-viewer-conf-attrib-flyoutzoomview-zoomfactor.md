---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '176'
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
   <td colname="col2"> <p>Anger hur komponenten hanterar små bilder. </p> <p>Om inställt på <span class="codeph"> 1</span> komponenten skalar upp huvudbilden så att den passar i huvudvyn. Dessutom skalas zoombilden upp så att den fyller det utfällbara fönsterområdet. </p> <p>Om inställt på <span class="codeph"> 0</span>små bilder visas med den ursprungliga upplösningen och centrerade i huvudvisningsområdet och inuti det utfällbara fönstret. Du kan konfigurera extra tomt utrymme runt bilden med en bakgrund eller liknande CSS-egenskap för <span class="codeph"> s7flyoutzoomview</span> och <span class="codeph"> s7flyoutzoom</span> CSS-klasser i huvudvyn respektive det utfällbara fönstret. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-e6310c8c4e8547689a5b48ceddb3671d}

Valfritt.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Exempel {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
