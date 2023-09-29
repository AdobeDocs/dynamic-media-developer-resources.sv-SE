---
title: coordN
description: Normaliserade koordinater. Används för att ange relativa positioner inom en bild, t.ex. förskjutningar av bilder eller beskärningsparametrar, normaliserade till bildens storlek.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# coordN{#coordn}

Normaliserade koordinater. Används för att ange relativa positioner inom en bild, t.ex. förskjutningar av bilder eller beskärningsparametrar, normaliserade till bildens storlek.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>koordinatförskjutning som normaliserats till en bilds storlek (verklig, verklig) </p></td> 
 </tr> 
</table>

Positiva värden flyttas mot det nedre högra hörnet.

Referenspositionen är ofta bildens mitt. I detta fall `0,0` motsvarar bildens mitt, `-0.5,-0.5` till det övre vänstra hörnet och `0.5,0.5` längst ned till höger.

Den används också för att ange bildstorlek eller rektangelstorlek i förhållande till storleken på lagret 0. I det här fallet måste värdet vara större än 0. 0 kan ange att ett visst standardvärde ska användas. Värdet för `1,1` anger en storlek som är lika med storleken på lager 0.
