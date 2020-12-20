---
description: 'null'
seo-description: 'null'
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
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
   <td colname="col2"> <p> Styr kvaliteten på förinlästa bildrutor. När den är inställd på <span class="codeph"> 1</span> inläses bildrutorna i hög kvalitet, vilket matchar komponentens storlek. Om <span class="codeph"> 0</span> är inställt på &lt;a0/&gt; läses endast den lågupplösta förhandsvisningspanelen in. </p> <p>Förhandsladdning med hög upplösning förbättrar slutanvändarens upplevelse, särskilt när automatisk rotation är aktiverat. Samtidigt resulterar det i långsammare starttid och högre nätverksförbrukning, så använd med försiktighet. När du använder en förinläsning med hög upplösning får de förinlästa bildrutorna alltid den ursprungliga upplösning som komponenten ursprungligen lästes in med. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
