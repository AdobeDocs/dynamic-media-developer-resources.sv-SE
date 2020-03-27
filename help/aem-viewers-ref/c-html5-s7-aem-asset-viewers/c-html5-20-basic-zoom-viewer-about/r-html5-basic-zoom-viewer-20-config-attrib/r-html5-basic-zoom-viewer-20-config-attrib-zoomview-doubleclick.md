---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.doubleClick
solution: Experience Manager
title: ZoomView.doubleClick
topic: Dynamic media
uuid: 676a13b5-4634-4233-8059-6effed6e2b5d
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

## Egenskaper {#section-50bcd15223174bb79ce08b31ea03d682}

Valfritt.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` på stationära datorer, på `zoomReset` pekenheter.

## Exempel {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
