---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av enkla klick/tryck för att zooma åtgärder. Om du anger <span class="codeph"> inget </span> inaktiveras zoomning med en klickning. Om den är inställd på <span class="codeph"> zoomning </span> när du klickar på bilden zoomas den i ett zoomsteg; CTRL+Click zoomar ut ett zoomsteg. Om du anger <span class="codeph"> reset </span> återställs zoomningen till den ursprungliga zoomnivån med ett enda klick på bilden. För <span class="codeph"> zoomReset </span> används reset om den aktuella zoomfaktorn är vid eller över den angivna gränsen, i annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`zoomReset` på stationära datorer,  `none` på pekenheter.

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
