---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---


# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> förinläsare</span></span> </p> </td> 
   <td colname="col2"> <p> Anger beteende för komponentförinläsning. När värdet är <span class="codeph"> -1</span> läses alla färgrutor in samtidigt när komponenten initieras eller resursen ändras. Om <span class="codeph"> 0</span> anges läses endast synliga färgrutor in. </p> <p><span class="codeph"> <span class="varname"> preloadnbr</span></span> definierar hur många osynliga rader/kolumner runt det synliga området som ska förinläsas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-e6310c8c4e8547689a5b48ceddb3671d}

Valfritt.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## Exempel {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
