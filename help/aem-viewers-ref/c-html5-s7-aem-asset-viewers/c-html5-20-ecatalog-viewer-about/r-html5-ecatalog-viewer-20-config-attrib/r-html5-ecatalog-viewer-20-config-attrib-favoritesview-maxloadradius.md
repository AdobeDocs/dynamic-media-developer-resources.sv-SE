---
title: FavoritesView.maxloadradius
description: FavoritesView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 6bbf75f1-96e7-496d-9f5c-6f449f76bfdd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Anger beteende för komponentförinläsning. </p> <p>När inställt på <span class="codeph"> -1</span>, läses alla miniatyrbilder in samtidigt när komponenten initieras eller resursen ändras. </p> <p>När inställt på <span class="codeph"> 0</span>, läses bara synliga miniatyrbilder in. </p> <p> När inställt på <span class="codeph"><span class="varname"> preloadnbr</span></span>kan du ange hur många osynliga rader runt det synliga området som är förinlästa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`
