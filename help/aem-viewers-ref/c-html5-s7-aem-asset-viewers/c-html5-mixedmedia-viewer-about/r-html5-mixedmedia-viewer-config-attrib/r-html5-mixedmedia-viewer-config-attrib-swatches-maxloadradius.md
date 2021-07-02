---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,Business Practitioner
exl-id: 06f493d7-18c9-4bb1-add6-a0dfd1a689bd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> förinläsare</span></span> </p> </td> 
   <td> <p>Anger beteende för komponentförinläsning. När värdet är <span class="codeph"> -1</span> läses alla färgrutor in samtidigt när komponenten initieras eller resursen ändras. </p> <p>Om <span class="codeph"> 0</span> anges läses endast synliga färgrutor in. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> definierar hur många osynliga rader/kolumner runt det synliga området som är förinlästa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
