---
title: Video360Player.preload
description: Anger om visningsprogrammet börjar läsa in videoinnehåll innan uppspelningen startar.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---

# Video360Player.preload{#video-player-preload}

Anger om visningsprogrammet börjar läsa in videoinnehåll innan uppspelningen startar.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Om inställt på <span class="codeph"> 1 </span>börjar videon att laddas ned direkt efter att resursen har ställts in. I annat fall startar förinläsningen endast efter att uppspelningen initierats av slutanvändaren eller ett API-anrop. </p> <p>Om inställt på <span class="codeph"> 0 </span>vissa funktioner fungerar kanske inte förrän uppspelningen startar. Sökåtgärden uppdaterar inte videobildrutan. Om förhandsvisningsbilden är inaktiverad visas den som ett tomt område i stället för som den första videobildrutan. </p> <p>Inaktivering av förinläsning av video kan ignoreras i vissa versioner av webbläsarna Internet Explorer 11 och Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
