---
description: Anger det bildformat som komponenten använder för att läsa in bilder från Image Server.
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,Business Practitioner
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 1%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Anger det bildformat som komponenten använder för att läsa in bilder från Image Server.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Om det angivna formatet slutar med <span class="codeph"> -alpha</span> återges bilderna som genomskinligt innehåll av komponenten. För alla andra bildformat hanterar komponenten bilder som ogenomskinliga. </p> <p>Observera att komponenten har en vit bakgrund som standard. För att göra den helt genomskinlig anger du därför CSS-egenskapen <span class="codeph"> background-color</span> som <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
