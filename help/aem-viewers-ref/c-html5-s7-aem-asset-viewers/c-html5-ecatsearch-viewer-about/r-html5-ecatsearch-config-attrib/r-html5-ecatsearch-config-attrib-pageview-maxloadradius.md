---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`förinläsare`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Anger beteende för komponentförinläsning. </p> <p>När den är inställd på <span class="codeph"> -1</span> läser komponenten in alla katalogbildrutor i förväg i ett inaktivt läge. </p> <p> När värdet är <span class="codeph"> 0</span> läser komponenten bara in den bildruta som är synlig, föregående bildruta och nästa bildruta. </p> <p>Ange <span class="codeph"><span class="varname"> förinläsare </span></span> för att definiera hur många osynliga bildrutor runt den bildruta som visas som förinlästa i ett inaktivt läge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-4b7952997f9240e581d21bcdb173f9af}

Valfritt.

## Standard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Exempel {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
