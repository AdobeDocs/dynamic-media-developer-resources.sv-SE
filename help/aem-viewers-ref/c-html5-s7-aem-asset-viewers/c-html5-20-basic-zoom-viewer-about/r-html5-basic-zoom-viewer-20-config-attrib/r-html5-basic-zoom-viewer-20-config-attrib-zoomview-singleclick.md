---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.singleClick
solution: Experience Manager
title: ZoomView.singleClick
topic: Dynamic media
uuid: 42327f03-269b-4d4e-a35d-2537ca3ba071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.singleClick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av enkla klick/tryck för att zooma åtgärder. Om du väljer <span class="codeph"> Ingen </span> inaktiveras zoomning med ett enda klick/tryck. Om inställningen är att <span class="codeph"> zooma in </span> zoomningen zoomas bilden i ett zoomsteg, CTRL+Click zoomar ut ett zoomsteg. Om du anger att du vill <span class="codeph"> återställa bilden </span> återställs zoomningen till den ursprungliga zoomnivån med ett enda klick. För <span class="codeph"> zoomReset </span>används reset om den aktuella zoomfaktorn är på eller över den angivna gränsen, i annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-50bcd15223174bb79ce08b31ea03d682}

Valfritt.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` på stationära datorer, på `none` pekenheter.

## Exempel {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
