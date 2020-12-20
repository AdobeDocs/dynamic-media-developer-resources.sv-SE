---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 2f44dc7f-ebed-4c74-b1ea-0b65655059fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av dubbelklicka/peka för att zooma åtgärder. Om du anger <span class="codeph"> inget </span> inaktiveras zoomning genom att dubbelklicka/trycka. Om den är inställd på <span class="codeph"> zoomning </span> när du klickar på bilden zoomas den i ett zoomsteg; CTRL+Click zoomar ut ett zoomsteg. Om du anger <span class="codeph"> reset </span> återställs zoomningen till den ursprungliga zoomnivån med ett enda klick på bilden. För <span class="codeph"> zoomReset </span> används reset om den aktuella zoomfaktorn är vid eller över den angivna gränsen, i annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` på stationära datorer,  `zoomReset` på pekenheter.

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
