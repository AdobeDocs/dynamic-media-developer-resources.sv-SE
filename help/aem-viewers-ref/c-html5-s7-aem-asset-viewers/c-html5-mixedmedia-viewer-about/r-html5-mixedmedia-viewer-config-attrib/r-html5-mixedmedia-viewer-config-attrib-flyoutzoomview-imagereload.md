---
title: FlyoutZoomView.imagereload
description: Konfigurerar hur komponenten hämtar nya bilder för huvud- och utfällningsvyn när storleken ändras.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 1%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Konfigurerar hur komponenten hämtar nya bilder för huvud- och utfällningsvyn när storleken ändras.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>När inställt på <span class="codeph"> 0 </span>läser komponenten inte in nya bilder när du ändrar storlek och bildupplösningen i den utfällbara vyn ändras inte. </p> <p>När inställt på <span class="codeph"> 1 </span> I kan du ange en eller flera breddbrytpunkter för bilden som läses in i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> brytpunkt, <span class="varname"> width </span>[; <span class="varname"> width </span>] </span> </p> </td> 
   <td colname="col2"> <p>Breddbrytpunkter för bilden som läses in i huvudvyn. Komponenten använder alltid den bästa passningsstorleken för den inledande inläsningen. När du har ändrat storlek hämtas alltid bilden i huvudvyn med bredden lika med närmaste större brytpunkt och den nedskalas på klienten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
