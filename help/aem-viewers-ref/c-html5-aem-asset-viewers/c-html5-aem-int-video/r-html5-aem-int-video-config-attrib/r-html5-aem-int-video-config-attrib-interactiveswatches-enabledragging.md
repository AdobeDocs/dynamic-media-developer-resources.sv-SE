---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: InteractiveSwatches.enabledragging
solution: Experience Manager
title: InteractiveSwatches.enabledragging
topic: Dynamic Media
uuid: 9a93e6b3-3441-4987-b9e6-a964dbf2247d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---


# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

Konfigurationsattribut för Interactive Video Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Aktiverar eller inaktiverar möjligheten för en användare att rulla färgrutorna med en mus eller genom att använda pekgester. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Är i intervallet <span class="codeph"> 0-1 </span> och är ett procentvärde för rörelsen i fel riktning av den faktiska hastigheten. </p> <p>Om <span class="codeph"> 1 </span> anges flyttas den med musen. </p> <p>Om <span class="codeph"> 0 </span> anges kan du inte gå i fel riktning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

