---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 06f493d7-18c9-4bb1-add6-a0dfd1a689bd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Anger beteende för komponentförinläsning. När inställt på <span class="codeph"> -1</span> alla färgrutor läses in samtidigt när komponenten initieras eller resursen ändras. </p> <p>När inställt på <span class="codeph"> 0</span> bara synliga färgrutor läses in. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> definierar hur många osynliga rader/kolumner runt det synliga området som är förinlästa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
