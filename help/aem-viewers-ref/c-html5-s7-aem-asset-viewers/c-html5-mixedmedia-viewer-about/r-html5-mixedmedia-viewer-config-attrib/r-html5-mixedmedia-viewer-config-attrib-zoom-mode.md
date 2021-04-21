---
description: Anger typ av zoominteraktion.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# zoomMode{#zoommode}

Anger typ av zoominteraktion.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kontinuerlig|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> kontinuerlig  </span> zoomning där bilden zoomas in gradvis när du klickar, dubbelknackar eller nyper i huvudvyn. Du måste zooma ut eller återställa zoomläget för att återgå till den inledande vyn. </p> <p> <span class="codeph"> inline  </span> möjliggör omedelbar zoomning, där den zoomade bilden visas direkt när du hovrar huvudvyn på skrivbordet eller när du håller pekfingret på en touchenhet, bilden återgår automatiskt till det ursprungliga läget när du flyttar musen från vyn eller släpper fingret. Observera att i <span class="codeph"> infogade </span>-läge förenklas kapslade bilduppsättningar och visas som enskilda miniatyrbilder. <span class="codeph"> aktiverar automatiskt  </span> inlineläge på skrivbordet och i helskärmsläge på touchenheter. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
