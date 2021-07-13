---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: InteractiveSwatches.enabledragging
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Developer,User
exl-id: 91c5eb52-40d9-40f6-8687-e68cb40b634e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
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
