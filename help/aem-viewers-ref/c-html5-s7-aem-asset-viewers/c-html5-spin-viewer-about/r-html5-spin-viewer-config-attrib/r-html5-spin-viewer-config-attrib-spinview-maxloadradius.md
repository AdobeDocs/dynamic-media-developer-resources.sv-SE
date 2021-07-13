---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Visningsprogram,SDK/API,snurra uppsättningar
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Representerar det maximala antalet bildrutor som ska förhandsladdas i varje riktning när SpinView är inaktiv. Värdet <span class="codeph"> -1</span> förläser alla bildrutor i uppsättningen. De förinlästa bildrutorna visas alltid med den ursprungliga upplösningen som SpinView ursprungligen lästes in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Styr kvaliteten på förinlästa bildrutor. När den är inställd på <span class="codeph"> 1</span> inläses bildrutorna i hög kvalitet, vilket matchar komponentens storlek. Om <span class="codeph"> 0</span> är inställt på  läses endast den lågupplösta förhandsvisningspanelen in. </p> <p>Förhandsladdning med hög upplösning förbättrar slutanvändarens upplevelse, särskilt när automatisk rotation är aktiverat. Samtidigt resulterar det i långsammare starttid och högre nätverksförbrukning, så använd med försiktighet. När du använder en förinläsning med hög upplösning får de förinlästa bildrutorna alltid den ursprungliga upplösning som komponenten ursprungligen lästes in med. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
