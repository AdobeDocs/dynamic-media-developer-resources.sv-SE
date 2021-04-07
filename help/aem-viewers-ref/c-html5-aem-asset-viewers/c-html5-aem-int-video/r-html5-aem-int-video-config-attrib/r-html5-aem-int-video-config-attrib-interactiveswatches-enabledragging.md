---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: InteractiveSwatches.enabledragging
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
exl-id: 91c5eb52-40d9-40f6-8687-e68cb40b634e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
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
