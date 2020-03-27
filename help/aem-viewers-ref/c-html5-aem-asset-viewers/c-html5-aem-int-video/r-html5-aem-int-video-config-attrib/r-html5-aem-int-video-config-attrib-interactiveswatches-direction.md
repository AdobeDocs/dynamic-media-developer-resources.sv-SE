---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
topic: Dynamic media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

Konfigurationsattribut för Interactive Video Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Anger hur färgrutor fylls i vyn. </p> <p>Ange till <span class="codeph"> vänster </span> för att ange fyllningsordningen från vänster till höger. </p> <p>Om du anger till <span class="codeph"> höger </span> inverteras ordningen så att vyn fylls i från höger till vänster, uppifrån och ned. </p> <p>När <span class="codeph"> auto </span> är inställt använder komponenten det högra läget när språkinställningen är inställd på " <span class="codeph"> ja </span>"; i annat fall används <span class="codeph"> left </span> . </p> </td> 
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

