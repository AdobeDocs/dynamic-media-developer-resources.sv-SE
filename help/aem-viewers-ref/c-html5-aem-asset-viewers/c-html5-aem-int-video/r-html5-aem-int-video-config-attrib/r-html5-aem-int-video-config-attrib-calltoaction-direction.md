---
title: CallToAction.direction
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# CallToAction.direction{#calltoaction-direction}

Konfigurationsattribut för Interactive Video Viewer.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Anger hur miniatyrbilder fylls i vyn. </p> <p>Ange till <span class="codeph"> vänster </span> för att ange fyllningsordningen från vänster till höger. </p> <p>Om värdet är <span class="codeph"> right </span> inverteras ordningen så att vyn fylls i från höger till vänster, uppifrån och ned. </p> <p>Ange som <span class="codeph"> auto </span> om du vill att komponenten ska använda högerläge när språkinställningen är inställd på <span class="codeph"> "ja" </span>; annars används <span class="codeph"> left </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
