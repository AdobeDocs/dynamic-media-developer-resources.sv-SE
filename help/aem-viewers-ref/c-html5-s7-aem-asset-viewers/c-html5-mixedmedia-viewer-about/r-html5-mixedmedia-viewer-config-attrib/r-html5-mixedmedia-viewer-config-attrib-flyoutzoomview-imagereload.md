---
description: Konfigurerar hur komponenten hämtar nya bilder för huvud- och utfällningsvyn när storleken ändras.
seo-description: Konfigurerar hur komponenten hämtar nya bilder för huvud- och utfällningsvyn när storleken ändras.
seo-title: FlyoutZoomView.imagerelload
solution: Experience Manager
title: FlyoutZoomView.imagerelload
topic: Dynamic media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagerelload{#flyoutzoomview-imagereload}

Konfigurerar hur komponenten hämtar nya bilder för huvud- och utfällningsvyn när storleken ändras.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`bredd`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Om värdet är <span class="codeph"> </span>0 läses inte nya bilder in när storleken ändras, och bildupplösningen i den utfällbara vyn ändras inte. </p> <p>Om värdet är <span class="codeph"> 1 </span> kan du ange en eller flera breddbrytpunkter för bilden som läses in i huvudvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> brytpunkt, <span class="varname"> bredd </span>[; <span class="varname"> width </span>] </span> </p> </td> 
   <td colname="col2"> <p>Breddbrytpunkter för bilden som läses in i huvudvyn. Komponenten använder alltid den bästa passningsstorleken för den inledande inläsningen. När du har ändrat storlek ser du till att bilden i huvudvyn alltid hämtas med bredden lika med närmaste större brytpunkt och nedskalad på klienten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
