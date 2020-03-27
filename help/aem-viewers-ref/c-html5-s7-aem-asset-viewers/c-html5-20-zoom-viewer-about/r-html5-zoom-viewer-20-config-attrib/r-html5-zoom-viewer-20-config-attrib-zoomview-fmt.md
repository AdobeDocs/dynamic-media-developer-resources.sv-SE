---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
topic: Dynamic media
uuid: 8e3e16a8-7b3c-4cb0-9c6d-a067bc7f6191
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. Om det angivna formatet slutar med <span class="codeph"> -alpha</span>återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Komponenten har som standard en vit bakgrund. För att göra den genomskinlig anger du därför CSS-egenskapen för <span class="codeph"> bakgrundsfärg</span> som <span class="codeph"> genomskinlig</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
