---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: CallToAction.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Konfigurationsattribut för Interactive Video Viewer.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> förinläsare</span></span> </p> </td> 
   <td colname="col2"> <p> Anger beteende för komponentförinläsning. </p> <p>När värdet är <span class="codeph"> -1</span> läses alla miniatyrbilder in samtidigt när komponenten initieras eller resursen ändras. </p> <p>Om <span class="codeph"> 0</span> anges läses endast synliga miniatyrer in. </p> <p>Ange <span class="codeph"><span class="varname"> som förinläsare</span></span> för att definiera hur många osynliga rader/kolumner runt det synliga området som ska förinläsas. </p> </td> 
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
