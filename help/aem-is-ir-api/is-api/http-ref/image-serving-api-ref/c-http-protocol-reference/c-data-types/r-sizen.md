---
description: Normaliserad storlek. Används för att ange bildstorlekar eller rektangulära storlekar, normaliserade i förhållande till storleken på lagret 0 eller någon annan bild.
seo-description: Normaliserad storlek. Används för att ange bildstorlekar eller rektangulära storlekar, normaliserade i förhållande till storleken på lagret 0 eller någon annan bild.
seo-title: sizeN
solution: Experience Manager
title: sizeN
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
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
