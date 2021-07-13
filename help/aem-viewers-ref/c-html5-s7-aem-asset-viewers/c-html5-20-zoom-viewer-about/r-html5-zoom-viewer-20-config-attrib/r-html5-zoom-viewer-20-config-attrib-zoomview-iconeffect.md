---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`countfadeautoHide `*][, *``*][, *``*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Gör att <span class="codeph">-ikoneffekten</span> kan visas högst upp i bilden när bilden är i ett återställningsläge och det är ett tecken på en tillgänglig åtgärd att interagera med bilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> antal</span></span> </p> </td> 
   <td colname="col2"> <p> Anger det maximala antalet gånger som ikoneffekten <span class="codeph"></span> visas och visas igen. Värdet <span class="codeph"> -1</span> anger att ikonen alltid visas oändligt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> tona</span></span> </p> </td> 
   <td colname="col2"> <p>Anger längden på animeringen för att visa eller dölja i sekunder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Anger antalet sekunder som ikoneffekten <span class="codeph"> ska vara helt synlig innan den döljs automatiskt. </span> Det vill säga, tiden efter att den intonade animeringen har slutförts men innan den uttonade animeringen börjar. Om du anger <span class="codeph"> 0</span> inaktiveras beteendet för att dölja automatiskt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
