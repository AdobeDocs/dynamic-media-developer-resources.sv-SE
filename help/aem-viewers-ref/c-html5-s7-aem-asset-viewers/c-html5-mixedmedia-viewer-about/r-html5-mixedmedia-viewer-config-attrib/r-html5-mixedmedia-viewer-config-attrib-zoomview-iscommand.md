---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: e2a9388d-c753-4988-9aa0-73c4d0428d67
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---


# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Kommandosträngen Bildsökning som används för att zooma bilden. Om det anges i URL:en måste alla förekomster av <span class="codeph"> &amp;</span> och <span class="codeph"> =</span> vara HTTP-kodade som <span class="codeph"> %26</span> respektive <span class="codeph"> %3D</span>. </p> <p> <p>Obs!  Kommandon för att ändra bildstorlek stöds inte. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Ingen.

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

När det anges i visningsprogrammets URL:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

När det anges i konfigurationsdata:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
