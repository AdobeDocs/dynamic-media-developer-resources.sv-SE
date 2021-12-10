---
title: PageView.doubleclick
description: PageView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av dubbelklicka/peka för att zooma åtgärder. Inställning till <span class="codeph"> ingen </span> inaktiverar dubbelklickning/knackning i zoomning. Om inställt på <span class="codeph"> zooma </span> klicka på bilden zoomas in ett zoomsteg, CTRL+Click zoomar ut ett zoomsteg. Inställning till <span class="codeph"> återställ </span> gör att ett enda klick på bilden återställer zoomningen till den ursprungliga zoomnivån. För <span class="codeph"> zoomReset </span>återställs om den aktuella zoomfaktorn är på eller utanför den angivna gränsen. I annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Valfritt.

## Standard {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` på stationära datorer, `zoomReset` på pekenheter.

## Exempel {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
