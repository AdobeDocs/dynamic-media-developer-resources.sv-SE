---
description: Anger om visningsprogrammet börjar läsa in videoinnehåll innan uppspelningen startar.
solution: Experience Manager
title: VideoPlayer.preload
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 1%

---

# VideoPlayer.preload{#videoplayer-preload}

Anger om visningsprogrammet börjar läsa in videoinnehåll innan uppspelningen startar.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Om värdet är <span class="codeph"> 1 </span> börjar videon laddas ned direkt efter att resursen har ställts in; I annat fall startar förinläsningen endast efter att uppspelningen initierats av slutanvändaren eller ett API-anrop. </p> <p>Om <span class="codeph"> 0 </span> är inställt på  kanske vissa funktioner inte fungerar förrän uppspelningen startar; sökåtgärden uppdaterar inte videobildrutan. Om förhandsvisningsbilden är inaktiverad visas den som ett tomt område i stället för som den första videobildrutan. </p> <p>Tänk på att inaktivering av förinläsning av video kan ignoreras i vissa versioner av webbläsarna Internet Explorer 11 och Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
