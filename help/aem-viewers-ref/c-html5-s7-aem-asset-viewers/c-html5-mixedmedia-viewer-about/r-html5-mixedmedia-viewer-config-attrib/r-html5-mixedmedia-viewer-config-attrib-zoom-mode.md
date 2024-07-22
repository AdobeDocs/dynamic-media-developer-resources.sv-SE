---
title: zoomMode
description: Anger typ av zoominteraktion.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# zoomMode{#zoommode}

Anger typ av zoominteraktion.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kontinuerlig|intern|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuous </span> aktiverar klassisk zoomning där bilden zoomas in gradvis när du klickar, dubbelknackar eller nyper i huvudvyn. Om du vill gå tillbaka till den inledande vyn zoomar du ut eller återställer zoomläget. klassen </p> <p> <span class="codeph"> inline </span> aktiverar omedelbar zoomning, där den zoomade bilden visas direkt när du hovrar huvudvyn på skrivbordet eller när du håller pekaren över en touchenhet. Bilden återgår automatiskt till det ursprungliga läget när du har flyttat musen från vyn eller släppt fingret. I <span class="codeph"> infogat </span>-läge förenklas kapslade bilduppsättningar och visas som enskilda miniatyrbilder. Klassen <span class="codeph"> auto </span> aktiverar infogat läge på skrivbordet och i kontinuerligt läge på touchenheter. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
