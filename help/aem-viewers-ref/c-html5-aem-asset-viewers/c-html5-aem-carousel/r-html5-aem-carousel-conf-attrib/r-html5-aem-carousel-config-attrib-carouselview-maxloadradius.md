---
title: CarouselView.maxloadradius
description: CarouselView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`förinläsare`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Anger beteende för komponentförinläsning. </p> <p>När den är inställd på <span class="codeph"> -1</span> läser komponenten in alla karusellbildrutor i förväg när den är inaktiv. </p> <p>När värdet är <span class="codeph"> 0</span> läser komponenten bara in den bildruta som är synlig, föregående och nästa bildruta. </p> <p><span class="codeph"><span class="varname"> preloader</span></span>definierar hur många osynliga bildrutor runt den bildruta som visas som förinlästa när den är inaktiv. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
