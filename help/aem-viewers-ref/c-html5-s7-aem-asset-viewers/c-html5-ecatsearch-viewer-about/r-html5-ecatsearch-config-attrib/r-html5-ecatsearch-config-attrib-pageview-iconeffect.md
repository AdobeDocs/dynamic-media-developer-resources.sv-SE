---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eb2196cb-b771-4828-8390-cd9e3fe6c57e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *`antal`*][, *`tona`*][, *`autoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
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

## Egenskaper {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Valfritt.

## Standard {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## Exempel {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
