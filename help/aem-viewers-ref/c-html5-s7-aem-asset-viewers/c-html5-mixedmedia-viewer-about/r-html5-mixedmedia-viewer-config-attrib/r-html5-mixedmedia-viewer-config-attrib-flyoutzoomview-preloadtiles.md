---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,Business Practitioner
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 2%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Ange <span class="codeph"> 1</span> om du vill aktivera förinläsning av den zoomade bilden. </p> <p>Ange <span class="codeph"> 0</span> om du vill läsa in zoombilden stegvis efter behov. </p> <p> <p>Obs!  Om du aktiverar det här alternativet kan det leda till betydligt högre bandbreddsanvändning, eftersom den zoomade bilden måste läsas in i sin helhet, även om användaren inte gör något för att zooma. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
