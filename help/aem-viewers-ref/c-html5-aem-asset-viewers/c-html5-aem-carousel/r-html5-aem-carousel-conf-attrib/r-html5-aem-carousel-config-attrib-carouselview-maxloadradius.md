---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> förinläsare</span></span> </p> </td> 
   <td> <p>Anger beteende för komponentförinläsning. </p> <p>När den är inställd på <span class="codeph"> -1</span> kommer komponenten att förhandsladda alla karusellbildrutor när den är inaktiv. </p> <p>Om <span class="codeph"> 0</span> anges läser komponenten bara in den bildruta som är synlig, föregående och nästa bildruta. </p> <p><span class="codeph"><span class="varname"> Med </span></span>förinläsningsfunktionen definieras hur många osynliga bildrutor runt den bildruta som visas som förinlästa när den är inaktiv. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
