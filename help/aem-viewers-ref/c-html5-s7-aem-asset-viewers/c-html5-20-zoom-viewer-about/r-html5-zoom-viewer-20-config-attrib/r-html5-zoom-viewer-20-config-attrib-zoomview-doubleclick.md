---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

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

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`reset` på stationära datorer,  `zoomReset` på pekenheter.

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
