---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b02f033d-be84-4cd0-b4bb-3ae9e424680c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 2%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Anger beteende för komponentförinläsning. När inställt på <span class="codeph"> -1</span> alla färgrutor läses in samtidigt när komponenten initieras eller resursen ändras. När inställt på <span class="codeph"> 0</span> bara synliga färgrutor läses in. </p> <p><span class="codeph"> <span class="varname"> preloadnbr</span></span> definierar hur många osynliga rader/kolumner runt det synliga området som är förinlästa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1`
