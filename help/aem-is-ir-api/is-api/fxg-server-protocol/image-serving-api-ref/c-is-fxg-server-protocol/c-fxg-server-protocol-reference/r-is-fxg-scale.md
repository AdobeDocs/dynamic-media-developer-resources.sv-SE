---
description: Skalförändra bilden. Skalar en bild utifrån faktor i förhållande till den högupplösta bilden.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 0%

---

# scale{#scale}

Skalförändra bilden. Skalar en bild utifrån faktor i förhållande till den högupplösta bilden.

`scale= *`faktor`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> faktor</span></span> </p> </td> 
  <td class="stentry"> <p>Skalfaktor (verklig, &gt;0). </p></td> 
 </tr> 
</table>

## Standard {#section-e9e53959b35844579f0f1d7721b71f8e}

Om inget anges används bilden utan skalning.

## Exempel {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
