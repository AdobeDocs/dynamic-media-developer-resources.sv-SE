---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: CallToAction.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 38ca592f-329c-4fd4-8dbc-a49000663e55
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 1%

---

# CallToAction.fmt{#calltoaction-fmt}

Konfigurationsattribut för Interactive Video Viewer.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. </p> <p>Om det angivna formatet slutar med "<span class="codeph"> -alpha</span>" återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilderna som ogenomskinliga. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
