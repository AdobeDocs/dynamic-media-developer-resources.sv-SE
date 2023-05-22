---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av dubbelklicka/peka för att zooma åtgärder. Inställning till <span class="codeph"> ingen </span> inaktiverar dubbelklickning/knackning i zoomning. Om inställt på <span class="codeph"> zooma </span> klicka på bilden zoomas in ett zoomsteg, CTRL+Click zoomar ut ett zoomsteg. Inställning till <span class="codeph"> återställ </span> gör att ett enda klick på bilden återställer zoomningen till den ursprungliga zoomnivån. För <span class="codeph"> zoomReset </span>återställs om den aktuella zoomfaktorn är på eller utanför den angivna gränsen. I annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` på stationära datorer, `zoomReset` på pekenheter.

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
