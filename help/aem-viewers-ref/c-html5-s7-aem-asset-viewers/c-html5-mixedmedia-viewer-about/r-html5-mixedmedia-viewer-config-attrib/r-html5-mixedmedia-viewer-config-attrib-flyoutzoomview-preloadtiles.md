---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
uuid: c9989916-d0f3-4268-932a-e12c693f5b74
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Mixa medieuppsättningar
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
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
