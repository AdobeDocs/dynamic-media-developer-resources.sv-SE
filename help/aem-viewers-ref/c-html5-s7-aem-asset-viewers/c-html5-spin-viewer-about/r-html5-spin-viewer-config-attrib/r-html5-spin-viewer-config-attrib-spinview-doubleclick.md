---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av åtgärder för att snurra genom att dubbelklicka/peka. Inställning till <span class="codeph"> ingen </span> inaktiverar rotation mellan dubbelklick och knackning. Om inställt på <span class="codeph"> zooma </span>, klickar du på att bilden snurrar i ett steg, CTRL+Click snurrar ut ett steg. Inställning till <span class="codeph"> återställ </span> gör att ett enda klick på bilden återställer rotationen till den ursprungliga rotationsnivån. För <span class="codeph"> zoomReset </span>, återställs om den aktuella rotationsfaktorn ligger på eller över den angivna gränsen, i annat fall används rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`reset` på stationära datorer, `zoomReset` på pekenheter.

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
