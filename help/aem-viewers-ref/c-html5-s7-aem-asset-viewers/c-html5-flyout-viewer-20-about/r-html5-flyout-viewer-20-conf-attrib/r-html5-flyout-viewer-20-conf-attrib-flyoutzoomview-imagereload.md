---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`bredd`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar hur komponenten hämtar nya bilder för huvud- och utfällningsvyn när storleken ändras. </p> <p>När den är inställd på <span class="codeph"> 0 </span> läser komponenten inte in nya bilder när storleken ändras; bildupplösningen i den utfällbara vyn ändras inte. </p> <p>Om du anger <span class="codeph"> 1 </span> kan du ange en eller flera breddbrytpunkter för bilden som läses in i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> brytpunkt,  <span class="varname"> bredd  </span>[;  <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p> Breddbrytpunkter för bilden som läses in i huvudvyn. Komponenten använder alltid den bästa passningsstorleken för den inledande inläsningen. När du har ändrat storlek ser det till att bilden i huvudvyn alltid hämtas med bredden lika med närmaste större brytpunkt och nedskalad på klienten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
