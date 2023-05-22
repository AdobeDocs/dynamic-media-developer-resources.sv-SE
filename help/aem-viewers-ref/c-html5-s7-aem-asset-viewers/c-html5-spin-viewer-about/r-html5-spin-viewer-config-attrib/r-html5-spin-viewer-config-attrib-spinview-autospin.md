---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`varaktighet`*][, *`riktning`*][, *`spin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Aktiverar eller inaktiverar den automatiska rotationsanimeringen. För att få bästa möjliga upplevelse av automatisk snurra rekommenderar vi att du läser in alla bildrutor i förväg genom att ställa in <span class="codeph"> maxloadradius</span> till <span class="codeph"> -1</span>. Observera dock att den här inställningen leder till ökad inläsningstid och ökad bandbreddsanvändning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> varaktighet</span></span> </p> </td> 
   <td colname="col2"> <p> Antalet sekunder per ett helt rotationsfält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> riktning</span></span> </p> </td> 
   <td colname="col2"> <p> Rotationsriktningen som är <span class="codeph"> 0</span> för spinning österut och <span class="codeph"> 1</span> för att snurra västerut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Antalet fullständiga rotationer som görs innan autospin stoppas. Talet är ett flyttal. Ange till <span class="codeph"> -1</span> för ett oändligt automatiskt snurra. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
