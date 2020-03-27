---
description: 'null'
seo-description: 'null'
seo-title: SpinView.doubleClick
solution: Experience Manager
title: SpinView.doubleClick
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.doubleClick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av åtgärder för att snurra genom att dubbelklicka/peka. Om du anger <span class="codeph"> Ingen </span> inaktiveras rotationsfunktionen för dubbelklick/tryck. Om den är inställd för att <span class="codeph"> zooma </span> när du klickar på bilden snurrar den i ett steg. CTRL+Click snurrar ut ett steg. Om du anger att du vill <span class="codeph"> återställa bilden </span> återställs rotationsnivån till den ursprungliga rotationsnivån med ett enda klick. För <span class="codeph"> zoomReset </span>används reset om den aktuella rotationsfaktorn är på eller över den angivna gränsen, annars används rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-924163cb2f6542499f49894becef7fb5}

Valfritt.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`reset` på stationära datorer, på `zoomReset` pekenheter.

## Exempel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
