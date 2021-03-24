---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 1%

---


# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|prickad</span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar återgivningsformatet för den angivna indikatorn. </p> <p>När den är inställd på <span class="codeph"> prickad</span> återges identiska indikatorer för alla sidor. </p> <p>Om <span class="codeph"> är inställt på numeric</span>, infogas ett 1-baserat sidnummer inuti varje indikatorelement. </p> <p>Åtgärdsläget <span class="codeph"> numerisk</span> stöds inte på enheter som kan hantera pekrörelser. I stället använder komponenten <span class="codeph"> prickade</span> på sådana enheter. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
