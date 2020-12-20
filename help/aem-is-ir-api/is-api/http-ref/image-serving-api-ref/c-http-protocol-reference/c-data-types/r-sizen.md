---
description: Normaliserad storlek. Används för att ange bildstorlekar eller rektangulära storlekar, normaliserade i förhållande till storleken på lagret 0 eller någon annan bild.
seo-description: Normaliserad storlek. Används för att ange bildstorlekar eller rektangulära storlekar, normaliserade i förhållande till storleken på lagret 0 eller någon annan bild.
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# sizeN{#sizen}

Normaliserad storlek. Används för att ange bildstorlekar eller rektangulära storlekar, normaliserade i förhållande till storleken på lagret 0 eller någon annan bild.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>normaliserad bredd och höjd i förhållande till en annan bild (verklig, verklig, större än 0) </p></td> 
 </tr> 
</table>

Både *nx* och *ny* måste vara större än 0. 0,0 kan indikera att en viss standardstorlek bör användas. 1,1 anger en storlek som är lika med referensbilden.
