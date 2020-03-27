---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.singleClick
solution: Experience Manager
title: ZoomView.singleClick
topic: Dynamic media
uuid: 919dd48e-b621-4dbb-9cae-f2d0f91f45a9
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

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`zoomReset` på stationära datorer, på `none` pekenheter.

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
