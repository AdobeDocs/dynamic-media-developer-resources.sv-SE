---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|prickad</span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar återgivningsformatet för den angivna indikatorn. </p> <p>När den är inställd på <span class="codeph"> prickad </span> återges identiska indikatorer för alla sidor. </p> <p>Om <span class="codeph"> är inställt på numeric</span>, infogas ett 1-baserat sidnummer inuti varje indikatorelement. </p> <p>Åtgärdsläget <span class="codeph"> numerisk</span> stöds inte på enheter som har pekrörelser. I stället använder komponenten <span class="codeph"> prickade</span> på sådana enheter. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
