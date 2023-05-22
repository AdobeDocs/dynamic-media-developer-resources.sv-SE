---
title: PageView.fmt
description: PageView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
source-git-commit: 5432393e265fba888579d700cf2f414dc4f680af
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. Om det angivna formatet slutar med <span class="codeph"> -alpha</span>återger komponenten bilder som genomskinligt innehåll. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Komponenten har som standard en vit bakgrund. För att göra den genomskinlig anger du <span class="codeph"> background-color</span> CSS-egenskap till <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Valfritt.

## Standard {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## Exempel {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
