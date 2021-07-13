---
description: Konfigurationsattribut för Carousel Viewer.
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# CarouselView.autoplay{#carouselview-autoplay}

Konfigurationsattribut för Carousel Viewer.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,varaktighet][,riktning]</span> </p> </td> 
   <td colname="col2"> <p> Anger på/av, varaktighet för att visa varje banderoll i karusellen och riktningen för automatisk slinga. </p> <p>Ange <span class="codeph"> 0</span> för automatisk loop av. </p> <p>Ange <span class="codeph"> 1</span> som automatisk loop på med varaktighet för övergång i sekunder som styrs av <span class="codeph"> duration</span>. </p> <p>Riktningen på den automatiska slingan styrs med <span class="codeph"> riktning</span>. Riktningen <span class="codeph"></span> har intervallet mellan <span class="codeph"> 1</span> höger-till-vänster och <span class="codeph"> 0</span> vänster-till-höger. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,9`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
