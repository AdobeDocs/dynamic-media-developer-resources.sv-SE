---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Anger beteende för komponentförinläsning. </p> <p>När inställt på <span class="codeph"> -1</span> komponenten läser in alla katalogbildrutor i förväg i ett inaktivt läge. </p> <p> När inställt på <span class="codeph"> 0</span> komponenten läser bara in den bildruta som är synlig, föregående och nästa bildruta. </p> <p>Ange <span class="codeph"><span class="varname"> preloadnbr</span></span> om du vill definiera hur många osynliga bildrutor runt den bildruta som visas som förinlästa i ett inaktivt läge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-4b7952997f9240e581d21bcdb173f9af}

Valfritt.

## Standard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Exempel {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
