---
title: FlyoutZoomView.fmt
description: Anger det bildformat som komponenten använder för att läsa in bilder från Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Anger det bildformat som komponenten använder för att läsa in bilder från Image Server.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Om det angivna formatet slutar med <span class="codeph"> -alpha</span>återger komponenten bilder som genomskinligt innehåll. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. </p> <p>Komponenten har som standard en vit bakgrund. För att göra den genomskinlig anger du <span class="codeph"> background-color</span> CSS-egenskap till <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
