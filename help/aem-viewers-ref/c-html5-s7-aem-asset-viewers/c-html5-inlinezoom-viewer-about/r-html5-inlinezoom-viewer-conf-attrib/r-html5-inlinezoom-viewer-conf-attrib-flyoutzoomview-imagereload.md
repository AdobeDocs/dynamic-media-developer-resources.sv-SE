---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar hur komponenten hämtar nya bilder för huvud- och utfällningsvyn när storleken ändras. </p> <p>Ange till <span class="codeph"> 0 </span>läser komponenten inte in nya bilder när du ändrar storlek och bildupplösningen i den utfällbara vyn ändras inte. </p> <p>Ange till <span class="codeph"> 1 </span> I kan du ange en eller flera breddbrytpunkter för bilden som läses in i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> brytpunkt, <span class="varname"> width </span>; <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p>Breddbrytpunkter för bilden som läses in i huvudvyn. </p> <p>Komponenten använder alltid den bästa passningsstorleken för den inledande inläsningen. När du har ändrat storlek hämtas alltid bilden i huvudvyn med den bredd som är lika med den närmaste större brytpunkten och som är nedskalad på klienten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-e6310c8c4e8547689a5b48ceddb3671d}

Valfritt.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Exempel {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
