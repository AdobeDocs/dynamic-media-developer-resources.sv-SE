---
description: Normaliserade koordinater. Används för att ange relativa positioner inom en bild, t.ex. förskjutningar av bilder eller beskärningsparametrar, normaliserade till bildens storlek.
seo-description: Normaliserade koordinater. Används för att ange relativa positioner inom en bild, t.ex. förskjutningar av bilder eller beskärningsparametrar, normaliserade till bildens storlek.
seo-title: coordN
solution: Experience Manager
title: coordN
topic: Scene7 Image Serving - Image Rendering API
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# coordN{#coordn}

Normaliserade koordinater. Används för att ange relativa positioner inom en bild, t.ex. förskjutningar av bilder eller beskärningsparametrar, normaliserade till bildens storlek.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>koordinatförskjutning som normaliserats till en bilds storlek (verklig, verklig) </p></td> 
 </tr> 
</table>

Positiva värden flyttas mot det nedre högra hörnet.

I många fall är referenspositionen bildens mitt. I det här fallet motsvarar 0,0 bildens mitt, -0,5,-0,5 till det övre vänstra hörnet och 0,5,0,5 till det nedre högra hörnet.

Används även för att ange bildstorlekar eller rektangelstorlek i förhållande till storleken på lagret 0. I det här fallet måste värdena vara större än 0. 0 kan ange att ett visst standardvärde ska användas. 1,1 anger en storlek som är lika med storleken för lager 0.
