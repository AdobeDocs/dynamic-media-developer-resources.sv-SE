---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
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

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
