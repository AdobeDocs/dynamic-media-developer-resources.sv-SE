---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 9b69f6d7-b7a1-42c6-98d7-80952b7f8b31
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Aktiverar eller inaktiverar en användares möjlighet att rulla i färgrutorna med en mus eller genom att använda pekgester </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Funktioner i <span class="codeph"> 0-1 </span> omfång. Det är en <span class="codeph"> % </span> värde för rörelse i fel riktning för den faktiska hastigheten. Om den är inställd på <span class="codeph"> 1 </span>flyttas den med musen. Om den är inställd på <span class="codeph"> 0 </span>kan du inte gå åt fel håll. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-e6310c8c4e8547689a5b48ceddb3671d}

Valfritt.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## Exempel {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
