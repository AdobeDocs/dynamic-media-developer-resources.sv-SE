---
title: coord
description: Pixelkoordinater. Används för att ange bildkoordinater i form av en pixelförskjutning i förhållande till det övre vänstra hörnet i en bild- eller lagerrektangel. Dessa koordinater används ofta i bildförskjutningar eller beskärningsparametrar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12ca4002-a540-4eb9-bb11-824d7cb41d30
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# coord{#coord}

Pixelkoordinater. Används för att ange bildkoordinater i form av en pixelförskjutning i förhållande till det övre vänstra hörnet i en bild- eller lagerrektangel. Dessa koordinater används ofta i bildförskjutningar eller beskärningsparametrar.

<table id="simpletable_A686120953124ACB8803CB9C877252AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> px </span> </span>, <span class="codeph"><span class="varname"> py </span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> px </span> </span>, <span class="codeph"><span class="varname"> py </span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> värden i pixlar (int) </p></td> 
 </tr> 
</table>

Koordinaten `0,0` refererar till bildens eller rektangelns övre vänstra hörn. Om du ökar värdena flyttas det nedåt till höger.
