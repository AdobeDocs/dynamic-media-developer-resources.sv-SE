---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: CallToAction.fmt
solution: Experience Manager
title: CallToAction.fmt
uuid: c85160e2-431f-42af-a468-c754bfe86ecd
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
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

