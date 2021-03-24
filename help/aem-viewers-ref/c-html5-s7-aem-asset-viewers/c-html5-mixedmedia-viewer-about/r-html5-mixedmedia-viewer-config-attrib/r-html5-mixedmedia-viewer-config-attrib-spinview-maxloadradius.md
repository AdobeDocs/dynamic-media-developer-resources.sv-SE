---
description: Representerar det maximala antalet bildrutor som ska förhandsladdas i varje riktning när SpinView är inaktiv.
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Mixa medieuppsättningar
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

Representerar det maximala antalet bildrutor som ska förhandsladdas i varje riktning när SpinView är inaktiv.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Värdet <span class="codeph"> -1</span> förläser alla bildrutor i uppsättningen. De förinlästa bildrutorna visas alltid med den ursprungliga upplösningen som SpinView ursprungligen lästes in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Styr kvaliteten på förinlästa bildrutor. </p> <p>När den är inställd på <span class="codeph"> 1</span> läses bildrutorna in med hög kvalitet och matchar komponentens storlek. </p> <p>Om <span class="codeph"> 0</span> är inställt på  läses endast den lågupplösta förhandsvisningspanelen in. </p> <p>Förhandsladdning med hög upplösning förbättrar slutanvändarens upplevelse, särskilt när automatisk rotation är aktiverat. Samtidigt resulterar det i långsammare starttid och högre nätförbrukning, så det bör användas med försiktighet. När högupplösta förinläsningar används, kommer de förinlästa bildrutorna alltid att ha den ursprungliga upplösning som komponenten ursprungligen lästes in med. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
