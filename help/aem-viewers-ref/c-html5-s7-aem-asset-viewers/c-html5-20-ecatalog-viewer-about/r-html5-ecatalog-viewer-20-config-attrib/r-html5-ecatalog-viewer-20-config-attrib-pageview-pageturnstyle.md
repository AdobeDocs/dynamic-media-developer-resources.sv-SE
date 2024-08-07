---
title: PageView.pageturnstyle
description: PageView.pageturnstyle
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 00706c64-c051-4b62-8194-61d0a1c565e9
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`

Styr komponentutseendet när `PageView.frametransition` är inställt på `turn` eller `auto` på skrivbordssystem.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth </span></span> </p> </td> 
   <td colname="col2"> <p> Bredden i pixlar på skuggan för sidavgränsaren som skiljer de vänstra och högra sidorna på uppslaget åt. Den styr också bredden på den skugga som körs bredvid den vändande sidan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> Skuggfärgen i RRGGBB-format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>Skuggopaciteten i intervallet <span class="codeph"> 0</span> till <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> Flagga (antingen <span class="codeph"> 0</span> eller <span class="codeph"> 1</span>) som aktiverar och inaktiverar kanten runt den vänstra sidan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor </span></span> </p> </td> 
   <td colname="col2"> <p> Kantfärgen i RRGGBB-format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor </span></span> </p> </td> 
   <td colname="col2"> <p> Färgen på den heltäckande fyllningen i komponentområdet som används vid sidvändningsanimering, i RRGGBB-format. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-54c634116cfe4f17813318e07539264c}

Valfritt.

## Standard {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## Exempel {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
