---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limit`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> gräns</span>]</span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar beteende som döljs automatiskt beroende på antal sidor och komponentstorlek vid körning. </p> <p> <span class="codeph"> 0</span> stänger av funktionen för att dölja automatiskt. </p> <p> <span class="codeph"> 1 </span> aktiverar funktionen för att dölja automatiskt. Komponenten döljer sina punkter om minst ett av följande villkor blir true: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">raden med punkter blir bredare än komponentbredden vid körning, eller </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">antalet sidor som angetts för den här komponenten överskrider gränsen som konfigurerats av parametern <span class="codeph"><span class="varname"> limit</span></span>. </li> 
     </ul> </p> <p> Om du anger <span class="codeph"><span class="varname">-gränsen</span></span> till <span class="codeph"> -1</span> inaktiveras det andra autodolda villkoret. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
