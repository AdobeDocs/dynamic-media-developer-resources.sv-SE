---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 1%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`antal`*][, *`tona`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Aktiverar <span class="codeph"> ikoneffekt</span> som visas högst upp i bilden när bilden är i ett återställningsläge och det är ett tecken på en tillgänglig åtgärd för att interagera med bilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> antal</span></span> </p> </td> 
   <td colname="col2"> <p> Anger maximalt antal gånger <span class="codeph"> ikoneffekt</span> visas och visas igen. Värdet för <span class="codeph"> -1</span> anger att ikonen alltid visas oändligt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> tona</span></span> </p> </td> 
   <td colname="col2"> <p>Anger längden på animeringen för att visa eller dölja i sekunder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Anger antalet sekunder som <span class="codeph"> ikoneffekt</span> förblir helt synlig innan den döljs automatiskt. Det vill säga, tiden efter att den intonade animeringen har slutförts men innan den uttonade animeringen börjar. En inställning för <span class="codeph"> 0</span> inaktiverar funktionen för att dölja automatiskt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
