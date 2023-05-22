---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av åtgärder för att snurra genom att dubbelklicka/peka. Inställning till <span class="codeph"> ingen </span> inaktiverar rotation mellan dubbelklick och knackning. Om inställt på <span class="codeph"> zooma </span>, klickar du på att bilden snurrar i ett steg, CTRL+Click snurrar ut ett steg. Inställning till <span class="codeph"> återställ </span> gör att ett enda klick på bilden återställer rotationen till den ursprungliga rotationsnivån. För <span class="codeph"> zoomReset </span>, återställs om den aktuella rotationsfaktorn ligger på eller över den angivna gränsen, i annat fall används rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` på stationära datorer, `zoomReset` på pekenheter.

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
