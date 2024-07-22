---
title: InteractiveSwatches.maxloadradius
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Konfigurationsattribut för Interactive Video Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`förinläsare`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Anger beteende för komponentförinläsning. </p> <p>När värdet är <span class="codeph"> -1</span> läses alla färgrutor in samtidigt när komponenten initieras eller resursen ändras. </p> <p>När värdet är <span class="codeph"> 0</span> läses endast synliga färgrutor in. </p> <p>Ange <span class="codeph"><span class="varname"> preloadBr</span></span> för att definiera hur många osynliga rader/kolumner runt det synliga området som är förinlästa. </p> </td> 
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
