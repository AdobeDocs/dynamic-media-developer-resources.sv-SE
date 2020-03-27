---
description: 'null'
seo-description: 'null'
seo-title: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
topic: Dynamic media
uuid: 4d9d161e-e39b-4607-9fb1-9dbfb06d7704
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som används av komponenten för att läsa in bilder från Image Server. Formatet är ett värde som stöds av Image Server och klientens webbläsare. </p> <p>Om bildformatet slutar med <span class="codeph"> -alpha</span>återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformatsvärden behandlas bilderna som ogenomskinliga. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
