---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
topic: Dynamic media
uuid: 914091e0-f026-423c-8c33-86a0284ac600
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> steg</span></span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar de in- och utzoomningsåtgärder som krävs för att öka eller minska upplösningen med en faktor på två. Upplösningsändringen för varje zoomåtgärd är 2^1 per steg. Ange <span class="codeph"> 0</span> om du vill zooma till full upplösning med en enda zoomåtgärd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Anger den maximala zoomupplösningen i förhållande till den högupplösta bilden. Standardvärdet är <span class="codeph"> 1.0</span>, som inte tillåter zoomning utöver full upplösning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
