---
description: Skalförändra bilden. Skalar en bild utifrån faktor i förhållande till den högupplösta bilden.
seo-description: Skalförändra bilden. Skalar en bild utifrån faktor i förhållande till den högupplösta bilden.
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '55'
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
