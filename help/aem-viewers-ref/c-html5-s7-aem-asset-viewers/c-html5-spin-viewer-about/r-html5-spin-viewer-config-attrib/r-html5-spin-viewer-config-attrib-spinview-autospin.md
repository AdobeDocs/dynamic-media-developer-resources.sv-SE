---
description: 'null'
seo-description: 'null'
seo-title: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
topic: Dynamic media
uuid: 9d24ed39-e4b9-442b-bc64-c77707ff69d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationDirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Aktiverar eller inaktiverar den automatiska rotationsanimeringen. För att få bästa möjliga upplevelse av automatisk rotation rekommenderar vi att du läser in alla bildrutor i förväg genom att ställa in <span class="codeph"> maxloadradius</span> på <span class="codeph"> -1</span>. Observera dock att detta leder till ökad inläsningstid och ökad bandbreddsanvändning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> varaktighet</span></span> </p> </td> 
   <td colname="col2"> <p> Antalet sekunder per ett helt rotationsfält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> riktning</span></span> </p> </td> 
   <td colname="col2"> <p> Rotationsriktningen som är <span class="codeph"> 0</span> för spinning österut och <span class="codeph"> 1</span> för spinning västerut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Antalet fullständiga rotationer som görs innan autospin stoppas. Talet är ett flyttal. Ange <span class="codeph"> -1</span> för en oändlig automatisk rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
