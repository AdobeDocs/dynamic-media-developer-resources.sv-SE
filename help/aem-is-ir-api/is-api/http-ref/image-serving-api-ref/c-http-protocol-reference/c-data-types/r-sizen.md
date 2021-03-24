---
description: Normaliserad storlek. Används för att ange bildstorlekar eller rektangulära storlekar, normaliserade i förhållande till storleken på lagret 0 eller någon annan bild.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
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
