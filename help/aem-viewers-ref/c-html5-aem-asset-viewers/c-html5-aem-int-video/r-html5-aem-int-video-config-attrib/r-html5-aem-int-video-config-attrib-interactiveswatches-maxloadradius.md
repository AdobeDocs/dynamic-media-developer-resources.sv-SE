---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: InteractiveSwatches.maxloadradius
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
topic: Dynamic media
uuid: 12391b8b-532f-4e68-ad60-4dbcc86d9e58
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 1%

---


# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Konfigurationsattribut för Interactive Video Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> förinläsare</span></span> </p> </td> 
   <td colname="col2"> <p> Anger beteende för komponentförinläsning. </p> <p>När värdet är <span class="codeph"> -1</span> läses alla färgrutor in samtidigt när komponenten initieras eller resursen ändras. </p> <p>Om <span class="codeph"> 0</span> anges läses endast synliga färgrutor in. </p> <p>Ange <span class="codeph"><span class="varname"> som förinläsare</span></span> för att definiera hur många osynliga rader/kolumner runt det synliga området som ska förinläsas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

