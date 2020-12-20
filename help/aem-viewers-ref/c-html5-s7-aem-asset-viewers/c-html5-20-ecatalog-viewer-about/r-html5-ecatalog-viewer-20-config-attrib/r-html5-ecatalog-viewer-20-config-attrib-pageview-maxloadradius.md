---
description: 'null'
seo-description: 'null'
seo-title: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: 425624c5-3cbe-4b63-8c6b-eff31f2ed919
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> förinläsare</span></span> </p> </td> 
   <td colname="col2"> <p>Anger beteende för komponentförinläsning. </p> <p>När den är inställd på <span class="codeph"> -1</span> läser komponenten in alla katalogbildrutor i förväg när den är inaktiv. </p> <p> Om <span class="codeph"> 0</span> anges läser komponenten bara in den bildruta som är synlig, föregående och nästa bildruta. </p> <p>Ange <span class="codeph"><span class="varname"> förinläsare</span></span> för att definiera hur många osynliga bildrutor runt den bildruta som visas som förinlästa i ett inaktivt läge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-4b7952997f9240e581d21bcdb173f9af}

Valfritt.

## Standard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Exempel {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
