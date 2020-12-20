---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 9eab6cb2-92a3-41d2-999a-254a7109d6b6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
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

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
