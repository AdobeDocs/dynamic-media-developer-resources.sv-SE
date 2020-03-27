---
description: Anger det bildformat som komponenten använder för att läsa in bilder från Image Server.
seo-description: Anger det bildformat som komponenten använder för att läsa in bilder från Image Server.
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 6f6a69b4-d581-44ff-b089-ce9d0d0170bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Anger det bildformat som komponenten använder för att läsa in bilder från Image Server.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Om det angivna formatet slutar med <span class="codeph"> -alpha</span>återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. </p> <p>Observera att komponenten har en vit bakgrund som standard. Om du vill göra den helt genomskinlig anger du därför CSS-egenskapen för <span class="codeph"> bakgrundsfärg</span> som <span class="codeph"> genomskinlig</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
