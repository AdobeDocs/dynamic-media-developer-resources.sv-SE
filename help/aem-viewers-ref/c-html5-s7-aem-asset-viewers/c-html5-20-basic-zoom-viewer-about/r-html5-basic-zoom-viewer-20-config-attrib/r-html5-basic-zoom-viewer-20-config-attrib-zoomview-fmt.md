---
title: ZoomView.fmt
description: ZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 7cb75d38-a577-4e06-b679-c4e00db5059a
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. Om det angivna formatet slutar med"-alfa" återges bilderna som genomskinligt innehåll. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Komponenten har som standard en vit bakgrund. Om du vill göra den genomskinlig anger du CSS-egenskapen för bakgrundsfärg som genomskinlig. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-50bcd15223174bb79ce08b31ea03d682}

Valfritt.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`jpeg`

## Exempel {#section-96e69b70365f461dae4399e49044ea2f}

`fmt=png-alpha`
