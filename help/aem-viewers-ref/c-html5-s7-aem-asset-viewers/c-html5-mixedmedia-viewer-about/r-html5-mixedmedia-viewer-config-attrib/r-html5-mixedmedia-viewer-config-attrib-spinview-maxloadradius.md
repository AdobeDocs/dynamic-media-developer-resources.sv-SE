---
title: SpinView.maxloadradius
description: Representerar det maximala antalet bildrutor som ska förhandsladdas i varje riktning när SpinView är inaktiv.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Representerar det maximala antalet bildrutor som ska förhandsladdas i varje riktning när SpinView är inaktiv.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Värdet för <span class="codeph"> -1</span> läser in alla bildrutor i uppsättningen i förväg. De förinlästa bildrutorna visas alltid med den ursprungliga upplösningen som SpinView ursprungligen lästes in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Styr kvaliteten på förinlästa bildrutor. </p> <p>När inställt på <span class="codeph"> 1</span> Bildrutorna läses in med hög kvalitet och matchar komponentens storlek. </p> <p>När inställt på <span class="codeph"> 0</span> bara lågupplösningspanelen läses in.</p> <p>Vid förinläsning med hög upplösning förbättras användarens upplevelse, särskilt när automatisk rotation är aktiverat. Samtidigt resulterar det i långsammare starttid och högre nätförbrukning, så det bör användas med försiktighet. När högupplösta förinläsningar används, kommer de förinlästa bildrutorna alltid att ha den ursprungliga upplösning som komponenten ursprungligen lästes in med. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
