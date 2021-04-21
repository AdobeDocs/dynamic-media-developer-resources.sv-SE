---
description: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`tal`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivera, begränsa eller inaktivera optimering för enheter där <span class="codeph"> devicePixelRatio</span> är större än <span class="codeph"> 1</span>, det vill säga enheter med högdensitetsvisning som iPhone4 och liknande enheter. </p> <p>Om den är aktiv begränsar komponenten storleken på IS-bildbegäran som om enheten bara hade ett pixelförhållande på <span class="codeph"> 1</span> och på så sätt minskar bandbredden. </p> <p>Se exemplet nedan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tal</span></span> </p> </td> 
   <td colname="col2"> <p> Om du använder inställningen <span class="codeph"> limit</span> aktiverar komponenten endast hög pixeldensitet upp till den angivna gränsen. </p> <p>Se exemplet nedan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
