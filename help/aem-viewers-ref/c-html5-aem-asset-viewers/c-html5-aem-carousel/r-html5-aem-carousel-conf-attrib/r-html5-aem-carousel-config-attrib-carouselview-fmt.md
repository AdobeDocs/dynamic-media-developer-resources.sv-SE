---
title: CarouselView.fmt
description: CarouselView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: a43ca095-2a59-4a0c-a460-f465cbd4ed5f
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# CarouselView.fmt{#carouselview-fmt}

`[CarouselView.|<containerId>_carouselView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. </p> <p>Om det angivna formatet slutar med <span class="codeph"> -alpha</span> återges bilderna som genomskinligt innehåll av komponenten. </p> <p>För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Komponenten har som standard en vit bakgrund. Om du vill göra den genomskinlig anger du CSS-egenskapen <span class="codeph"> background-color </span> som <span class="codeph"> transparent </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
