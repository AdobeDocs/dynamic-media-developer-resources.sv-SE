---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic,Visningsprogram,SDK/API,snurra uppsättningar
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av åtgärder för att snurra genom att dubbelklicka/peka. Om du anger <span class="codeph"> inget </span> inaktiveras rotationsklickning. Om <span class="codeph"> är inställt på zoom </span> klickar du på bilden snurrar i ett steg; CTRL+Click snurrar ut ett steg. Om du ställer in på <span class="codeph"> reset </span> återställs rotationsnivån till den ursprungliga rotationsnivån med ett enda klick på bilden. För <span class="codeph"> zoomReset </span> används reset om den aktuella rotationsfaktorn är på eller utanför den angivna gränsen, annars används rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`reset` på stationära datorer,  `zoomReset` på pekenheter.

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
