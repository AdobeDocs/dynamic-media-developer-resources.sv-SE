---
title: Video360Player.iconeffect
description: Konfigurationsattribut för Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Konfigurationsattribut för Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Gör att IconEffect kan visas ovanpå videon när videon är i pausat läge. På vissa enheter används inbyggda kontroller. I sådana fall ignoreras modifieraren <span class="codeph">iconeffect</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> antal</span></span> </p> </td> 
   <td colname="col2"> <p> Anger det maximala antalet gånger som IconEffect visas och visas igen. Värdet <span class="codeph"> -1</span> anger att ikonen visas oändligt igen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tonad</span></span> </p> </td> 
   <td colname="col2"> <p> Anger hur länge animeringen ska visas eller döljas, i sekunder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Anger antalet sekunder som IconEffect ska vara helt synlig innan den döljs automatiskt. Det vill säga, tiden efter att animeringen har tonats in och innan den uttonade animeringen börjar. Ange till <span class="codeph"> 0</span> om du vill inaktivera funktionen för att dölja automatiskt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
