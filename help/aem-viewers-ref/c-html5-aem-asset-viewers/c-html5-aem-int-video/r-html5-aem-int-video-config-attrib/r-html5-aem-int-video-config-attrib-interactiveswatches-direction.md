---
title: InteractiveSwatches.direction
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Konfigurationsattribut för Interactive Video Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Anger hur färgrutor fylls i vyn. </p> <p>Ange till <span class="codeph"> vänster </span> för att ange fyllningsordningen från vänster till höger. </p> <p>Ange till <span class="codeph"> höger </span> inverterar ordningen så att vyn fylls i från höger till vänster, uppifrån och ned. </p> <p>När <span class="codeph"> auto </span> är inställt används rätt läge för komponenten när språkområdet är inställt på <span class="codeph"> ja </span>"; i annat fall, <span class="codeph"> vänster </span> används. </p> </td> 
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
