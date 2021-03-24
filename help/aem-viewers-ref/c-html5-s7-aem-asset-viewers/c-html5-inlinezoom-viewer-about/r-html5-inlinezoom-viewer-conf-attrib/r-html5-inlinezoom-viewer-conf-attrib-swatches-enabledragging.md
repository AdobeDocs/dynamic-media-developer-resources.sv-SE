---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Textbunden zoom
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---


# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td> <p> Aktiverar eller inaktiverar en användares möjlighet att rulla i färgrutorna med en mus eller genom att använda pekgester </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> Funktioner i <span class="codeph"> 0-1 </span>-intervallet. Det är ett <span class="codeph"> % </span>-värde för förflyttning i fel riktning av den faktiska hastigheten. Om den är inställd på <span class="codeph"> 1 </span> flyttas den med musen. Om det är inställt på <span class="codeph"> 0 </span> kan du inte gå i fel riktning alls. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-e6310c8c4e8547689a5b48ceddb3671d}

Valfritt.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## Exempel {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
