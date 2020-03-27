---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: InteractiveSwatches.fmt
solution: Experience Manager
title: InteractiveSwatches.fmt
topic: Dynamic media
uuid: 0a30c913-39d1-4521-b65c-f2b3879f6928
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Konfigurationsattribut för Interactive Video Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. </p> <p>Om det angivna formatet slutar med "<span class="codeph"> -alpha</span>" återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilderna som ogenomskinliga. Observera att komponenten har en vit bakgrund som standard. Om du vill göra den helt genomskinlig anger du därför CSS-egenskapen för bakgrundsfärg <span class="codeph"> som</span> genomskinlig <span class="codeph"></span>. </p> </td> 
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

