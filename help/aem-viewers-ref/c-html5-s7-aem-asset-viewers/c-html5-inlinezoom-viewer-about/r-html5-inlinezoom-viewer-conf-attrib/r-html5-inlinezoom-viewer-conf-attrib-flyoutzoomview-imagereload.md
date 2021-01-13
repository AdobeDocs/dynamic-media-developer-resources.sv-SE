---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`bredd`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar hur komponenten hämtar nya bilder för huvud- och utfällningsvyn när storleken ändras. </p> <p>Ange <span class="codeph"> 0 </span>, komponenten läser inte in nya bilder vid storleksändring och bildupplösningen i den utfällbara vyn ändras inte. </p> <p>Om du anger <span class="codeph"> 1 </span> kan du ange en eller flera breddbrytpunkter för bilden som läses in i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> brytpunkt,  <span class="varname"> bredd  </span>;  <span class="varname"> width  </span> </span> </p> </td> 
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
