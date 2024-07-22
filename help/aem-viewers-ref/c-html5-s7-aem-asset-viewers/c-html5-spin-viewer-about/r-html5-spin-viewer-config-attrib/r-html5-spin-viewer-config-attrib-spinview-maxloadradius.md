---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> värde </span></span> </p> </td> 
   <td colname="col2"> <p> Representerar det maximala antalet bildrutor som ska förhandsladdas i varje riktning när SpinView är inaktiv. Värdet <span class="codeph"> -1</span> läser in alla bildrutor i uppsättningen i förväg. De förinlästa bildrutorna visas alltid med den ursprungliga upplösningen som SpinView ursprungligen lästes in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes </span></span> </p> </td> 
   <td colname="col2"> <p> Styr kvaliteten på förinlästa bildrutor. När värdet är <span class="codeph"> 1</span> inläses bildrutor med hög kvalitet, vilket matchar komponentens storlek. Om värdet är <span class="codeph"> 0</span> läses endast den lågupplösta förhandsvisningspanelen in. </p> <p>Förhandsladdning med hög upplösning förbättrar slutanvändarens upplevelse, särskilt när automatisk rotation är aktiverat. Samtidigt resulterar det i långsammare starttid och högre nätverksförbrukning, så använd med försiktighet. När du använder en förinläsning med hög upplösning får de förinlästa bildrutorna alltid den ursprungliga upplösning som komponenten ursprungligen lästes in med. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
