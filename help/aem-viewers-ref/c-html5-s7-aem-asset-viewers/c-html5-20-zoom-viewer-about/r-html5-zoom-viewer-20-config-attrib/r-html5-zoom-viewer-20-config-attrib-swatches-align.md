---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3cb91483-de8c-4d5c-9b46-7026c5001f3a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Anger den interna justeringen (ankarpunkten) för färgrutebehållaren i komponentområdet. I Färgrutor ändras storleken på den interna miniatyrbehållaren så att endast ett helt antal färgrutor visas. Därför finns det viss utfyllnad mellan den interna behållaren och de externa komponentgränserna. Det här kommandot anger hur den interna färgrutebehållaren placeras inuti komponenten.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> vänster|center|höger</span> </p> </td> 
   <td> <p> Anger justeringen för de vågräta färgrutorna. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td> <p> Anger justeringen för de lodräta färgrutorna. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`center,center`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`align=left,top`
