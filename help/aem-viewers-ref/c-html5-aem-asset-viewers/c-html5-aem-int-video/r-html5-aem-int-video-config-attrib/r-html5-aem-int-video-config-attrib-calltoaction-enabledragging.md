---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: CallToAction.enabledragging
solution: Experience Manager
title: CallToAction.enabledragging
topic: Dynamic media
uuid: efb272b5-e30e-44d5-9dec-0529b1074ed2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

Konfigurationsattribut för Interactive Video Viewer.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Aktiverar eller inaktiverar möjligheten för en användare att rulla miniatyrbilderna med en mus eller genom att använda pekgester. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span></span> </p> </td> 
   <td colname="col2"> <p> Är i <span class="codeph"> </span> intervallet 0-1 och är ett procentvärde för rörelsen i fel riktning av den faktiska hastigheten. </p> <p>Om inställningen är <span class="codeph"> 1 flyttas </span> den med musen. </p> <p>Om värdet är <span class="codeph"> </span> 0 kan du inte flytta i fel riktning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

