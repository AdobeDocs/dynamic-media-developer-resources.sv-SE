---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
topic: Dynamic media
uuid: c8adabf9-ccbf-4a46-b1e7-b4cb58d4e606
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 1%

---


# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *`countfadeautoHide `*][, *``*][, *``*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
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

## Egenskaper {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Valfritt.

## Standard {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## Exempel {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
