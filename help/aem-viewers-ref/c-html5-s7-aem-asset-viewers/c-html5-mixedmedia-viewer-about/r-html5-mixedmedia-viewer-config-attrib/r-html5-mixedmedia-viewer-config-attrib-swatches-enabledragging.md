---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fd432573-677f-4c46-9cc1-88089496ce75
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

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
   <td> <p> Funktioner i intervallet <span class="codeph"> 0-1 </span>. Det är ett <span class="codeph"> % </span>-värde för rörelse i fel riktning av den faktiska hastigheten. Om den är inställd på <span class="codeph"> 1 </span> flyttas den med musen. Om värdet är <span class="codeph"> 0 </span> kan du inte gå i fel riktning alls. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
