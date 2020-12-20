---
description: 'null'
seo-description: 'null'
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av åtgärder för att snurra genom att dubbelklicka/peka. Om du anger <span class="codeph"> inget </span> inaktiveras rotationsklickning. Om <span class="codeph"> är inställt på zoom </span> klickar du på bilden snurrar i ett steg; CTRL+Click snurrar ut ett steg. Om du ställer in på <span class="codeph"> reset </span> återställs rotationsnivån till den ursprungliga rotationsnivån med ett enda klick på bilden. För <span class="codeph"> zoomReset </span> används reset om den aktuella rotationsfaktorn är på eller utanför den angivna gränsen, annars används rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` på stationära datorer,  `zoomReset` på pekenheter.

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
