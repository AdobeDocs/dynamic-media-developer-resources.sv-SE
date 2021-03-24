---
description: Konfigurationsattribut för Carousel Viewer.
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
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

