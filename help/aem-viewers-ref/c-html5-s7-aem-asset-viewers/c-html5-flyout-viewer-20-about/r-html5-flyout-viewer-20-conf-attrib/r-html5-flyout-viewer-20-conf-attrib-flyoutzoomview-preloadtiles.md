---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Flyout
role: Developer,User
exl-id: 34c8c7b9-0369-4d13-95f5-ad129e913453
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
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

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
