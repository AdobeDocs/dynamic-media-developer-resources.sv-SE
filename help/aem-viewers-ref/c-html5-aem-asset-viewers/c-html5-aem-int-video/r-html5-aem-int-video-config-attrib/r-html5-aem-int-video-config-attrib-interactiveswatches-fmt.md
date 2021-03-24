---
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
title: InteractiveSwatches.fmt
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---


# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Konfigurationsattribut för Interactive Video Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. </p> <p>Om det angivna formatet slutar med "<span class="codeph"> -alpha</span>" återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilderna som ogenomskinliga. Observera att komponenten har en vit bakgrund som standard. För att göra den helt genomskinlig anger du därför CSS-egenskapen <span class="codeph"> background-color</span> som <span class="codeph"> transparent</span>. </p> </td> 
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

