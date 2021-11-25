---
title: PanoramicView.fmt
description: Anger det bildformat som används av komponenten för att läsa in bilder från Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PanoramicView.fmt{#panoramicview-fmt}

Anger det bildformat som används av komponenten för att läsa in bilder från Image Server. Om det angivna formatet slutar med&quot;-alpha&quot; återges bilderna som genomskinliga av komponenten. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Observera att komponenten som standard har en genomskinlig bakgrund. För att göra den ogenomskinlig anger du `background-color` CSS-egenskap till `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Anger det bildformat som ska användas av komponenten för att läsa in bilder från Image Server. Om det angivna formatet slutar med"-alfa" återges bilderna som genomskinligt innehåll av komponenten. för alla andra bildformat hanterar komponenten bilder som ogenomskinliga. Observera att komponenten har genomskinlig bakgrund som standard, så om du vill använda ogenomskinlig anger du CSS-egenskapen background-color till önskad färg. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
