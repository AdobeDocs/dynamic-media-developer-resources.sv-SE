---
title: FlyoutZoomView.fmt
description: FlyoutZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 4e1ce754-6967-492b-a617-764ee3ec3a55
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 1%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som ska användas av komponenten för att läsa in bilder från Image Server. Om det angivna formatet slutar med <span class="codeph"> "-alpha"</span>återger komponenten bilder som genomskinligt innehåll. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Komponenten har som standard en vit bakgrund. För att göra den genomskinlig anger du därför <span class="codeph"> background-color</span> CSS-egenskap till <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`
