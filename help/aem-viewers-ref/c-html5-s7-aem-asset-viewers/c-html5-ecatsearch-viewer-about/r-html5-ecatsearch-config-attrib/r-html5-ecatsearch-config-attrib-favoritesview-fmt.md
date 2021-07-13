---
description: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Developer,User
exl-id: 9ec5ed03-1d8f-4e67-a9a3-bdf160b105c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# FavoritesView.fmt{#favoritesview-fmt}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som används av komponenten för att läsa in bilder från Image Server. Formatet är ett värde som stöds av Image Server och klientens webbläsare. </p> <p>Om bildformatet slutar med <span class="codeph"> -alpha</span> återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformatsvärden behandlas bilderna som ogenomskinliga. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
