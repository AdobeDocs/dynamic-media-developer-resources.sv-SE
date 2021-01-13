---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
topic: Dynamic media
uuid: bc68fc0a-94bf-42b3-a386-e0a248e8445c
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
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

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,1`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
