---
description: Normaliserad storlek. Används för att ange bildstorlekar eller rektangulära storlekar, normaliserade i förhållande till storleken på lagret 0 eller någon annan bild.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
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
