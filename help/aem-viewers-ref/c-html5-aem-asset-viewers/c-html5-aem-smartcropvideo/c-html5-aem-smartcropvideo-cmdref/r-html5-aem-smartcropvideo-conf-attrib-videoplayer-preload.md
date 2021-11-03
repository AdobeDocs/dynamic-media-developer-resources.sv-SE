---
description: Anger om visningsprogrammet börjar läsa in videoinnehåll innan uppspelningen startar.
solution: Experience Manager
title: SmartCropVideoPlayer.preload
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

Anger om visningsprogrammet börjar läsa in videoinnehåll innan uppspelningen startar.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Om inställt på <span class="codeph"> 1 </span> videon börjar laddas ned direkt efter att resursen har ställts in, I annat fall startar förinläsningen endast efter att uppspelningen initierats av slutanvändaren eller ett API-anrop. </p> <p>Om inställt på <span class="codeph"> 0 </span> vissa funktioner kanske inte fungerar förrän uppspelningen startar, sökåtgärden uppdaterar inte videobildrutan. Om förhandsvisningsbilden är inaktiverad visas den som ett tomt område i stället för som den första videobildrutan. </p> <p>Tänk på att inaktivering av förinläsning av video kan ignoreras i vissa versioner av webbläsarna Internet Explorer 11 och Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
