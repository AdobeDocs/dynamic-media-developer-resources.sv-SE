---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

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

[!DNL `reset`] på stationära datorer, [!DNL `zoomReset`] på pekenheter.

## Exempel {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
