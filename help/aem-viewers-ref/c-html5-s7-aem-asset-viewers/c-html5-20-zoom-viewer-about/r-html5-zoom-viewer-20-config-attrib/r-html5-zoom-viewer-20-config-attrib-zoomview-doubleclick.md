---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.doubleClick
solution: Experience Manager
title: ZoomView.doubleClick
topic: Dynamic media
uuid: 8dabc31c-ec7e-4dc0-b528-4f3f43f46721
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.doubleClick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av dubbelklicka/peka för att zooma åtgärder. Om du anger <span class="codeph"> Ingen </span> inaktiveras zoomning med dubbelklick/tryck. Om inställningen är att <span class="codeph"> zooma in </span> zoomningen zoomas bilden i ett zoomsteg, CTRL+Click zoomar ut ett zoomsteg. Om du anger att du vill <span class="codeph"> återställa bilden </span> återställs zoomningen till den ursprungliga zoomnivån med ett enda klick. För <span class="codeph"> zoomReset </span>används reset om den aktuella zoomfaktorn är på eller över den angivna gränsen, i annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`reset` på stationära datorer, på `zoomReset` pekenheter.

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
