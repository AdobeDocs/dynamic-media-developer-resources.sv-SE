---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 570a9cca-17fa-44d5-b3bb-66ec19453cbc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som ska användas av komponenten för att läsa in bilder från Image Server. Om det angivna formatet slutar med <span class="codeph"> -alpha</span>återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. </p> <p>Observera att komponenten har en vit bakgrund som standard. Om du vill göra den helt genomskinlig anger du därför CSS-egenskapen för bakgrundsfärg <span class="codeph"> som</span> genomskinlig <span class="codeph"></span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-e6310c8c4e8547689a5b48ceddb3671d}

Valfritt.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Exempel {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
