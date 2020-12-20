---
description: 'null'
seo-description: 'null'
seo-title: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
topic: Dynamic media
uuid: 61e6372c-bab9-4aac-a8a1-dffecc2e4903
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 1%

---


# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Anger det bildformat som komponenten använder för att läsa in bilder från Image Server. Om det angivna formatet slutar med <span class="codeph"> -alpha</span> återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Observera att komponenten har en vit bakgrund som standard. Om du vill göra bakgrunden genomskinlig anger du därför CSS-egenskapen <span class="codeph"> background-color</span> till <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha`
