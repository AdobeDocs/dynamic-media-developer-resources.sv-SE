---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

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

[!DNL `1`]

## Exempel {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
