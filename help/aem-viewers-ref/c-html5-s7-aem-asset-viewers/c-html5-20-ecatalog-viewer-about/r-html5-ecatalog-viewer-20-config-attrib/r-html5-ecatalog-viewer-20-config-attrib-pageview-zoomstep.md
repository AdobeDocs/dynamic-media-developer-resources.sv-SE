---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 1%

---


# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> steg</span></span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar antalet in- och utzoomningsåtgärder som krävs för att öka eller minska upplösningen med en faktor på två. Upplösningsändringen för varje zoomåtgärd är 2^1 per steg. Ange <span class="codeph"> 0</span> om du vill zooma till full upplösning med en enda zoomåtgärd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Anger den maximala zoomupplösningen i förhållande till den högupplösta bilden. Standardvärdet är <span class="codeph"> 1.0</span>, som inte tillåter zoomning utöver full upplösning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-636d35a4791447039f1902973f568320}

Valfritt.

## Standard {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Exempel {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
