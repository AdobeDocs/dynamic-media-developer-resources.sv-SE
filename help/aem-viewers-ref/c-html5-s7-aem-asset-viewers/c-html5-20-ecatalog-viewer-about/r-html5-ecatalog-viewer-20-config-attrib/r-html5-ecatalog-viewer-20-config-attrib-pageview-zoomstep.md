---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`steg`*[, *`limit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> steg</span></span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar antalet in- och utzoomningsåtgärder som krävs för att öka eller minska upplösningen med en faktor på två. Upplösningsändringen för varje zoomåtgärd är 2^1 per steg. Ange till <span class="codeph"> 0</span> för att zooma till full upplösning med en enda zoomåtgärd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Anger den maximala zoomupplösningen i förhållande till den högupplösta bilden. Standardvärdet är <span class="codeph"> 1.0</span>som inte tillåter zoomning utöver full upplösning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-636d35a4791447039f1902973f568320}

Valfritt.

## Standard {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Exempel {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
