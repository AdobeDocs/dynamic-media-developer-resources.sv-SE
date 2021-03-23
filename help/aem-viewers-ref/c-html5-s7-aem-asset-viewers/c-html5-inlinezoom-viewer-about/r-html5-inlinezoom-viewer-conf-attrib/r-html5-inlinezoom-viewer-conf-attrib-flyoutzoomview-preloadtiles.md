---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
uuid: 8e989ca7-1ef7-4758-b6b9-c447d7647d1d
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Textbunden zoom
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Ange <span class="codeph"> 1</span> om du vill aktivera förinläsning av den zoomade bilden, eller ange <span class="codeph"> 0</span> om du vill läsa in zoombilden stegvis efter behov. </p> <p> <p>Obs!  Om du aktiverar det här alternativet kan det leda till betydligt högre bandbreddsanvändning. Den zoomade bilden läses in i sin helhet, även om användaren inte startar en zoomåtgärd. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-e6310c8c4e8547689a5b48ceddb3671d}

Valfritt.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Exempel {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
