---
title: CallToAction.maxloadradius
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Konfigurationsattribut för Interactive Video Viewer.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Anger beteende för komponentförinläsning. </p> <p>När inställt på <span class="codeph"> -1</span> alla miniatyrbilder läses in samtidigt när komponenten initieras eller resursen ändras. </p> <p>När inställt på <span class="codeph"> 0</span> bara synliga miniatyrer läses in. </p> <p>Ange till <span class="codeph"><span class="varname"> preloadnbr</span></span> om du vill definiera hur många osynliga rader/kolumner runt det synliga området som är förinlästa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`-1`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
