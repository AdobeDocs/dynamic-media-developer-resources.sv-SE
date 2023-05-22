---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`antal`*][, *`tona`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Gör att IconEffect kan visas högst upp i bilden när bilden är i ett återställningsläge, vilket tyder på en tillgänglig åtgärd för interaktion med bilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> antal</span> </span> </p> </td> 
   <td colname="col2"> <p> Anger det maximala antalet gånger som IconEffect visas och visas igen. Värdet för <span class="codeph"> -1</span> anger att ikonen alltid visas oändligt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tona</span> </span> </p> </td> 
   <td colname="col2"> <p>Anger längden på animeringen för att visa eller dölja i sekunder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Anger antalet sekunder som IconEffect ska vara helt synlig innan den döljs automatiskt. Det vill säga, tiden efter att den intonade animeringen har slutförts men innan den uttonade animeringen börjar. En inställning för <span class="codeph"> 0</span> inaktiverar funktionen för att dölja automatiskt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-50bcd15223174bb79ce08b31ea03d682}

Valfritt.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Exempel {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
