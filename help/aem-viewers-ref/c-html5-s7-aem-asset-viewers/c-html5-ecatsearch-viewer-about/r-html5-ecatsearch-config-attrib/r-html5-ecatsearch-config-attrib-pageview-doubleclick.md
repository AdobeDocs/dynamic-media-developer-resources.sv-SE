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
   <td colname="col2"> <p> Konfigurerar mappningen av dubbelklicka/peka för att zooma åtgärder. Om du anger <span class="codeph"> none </span> inaktiveras zoomning med dubbelklick/tryck. Om inställningen är <span class="codeph"> zoomning </span>, zoomas bilden in i ett zoomsteg, om du klickar på bilden zoomas Ctrl+klickar du ett zoomsteg. Om du anger <span class="codeph"> reset </span> återställs zoomningen till den ursprungliga zoomnivån med ett enda klick på bilden. För <span class="codeph"> zoomReset </span> används reset om den aktuella zoomfaktorn är vid eller över den angivna gränsen, i annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Valfritt.

## Standard {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] på stationära datorer; [!DNL `zoomReset`] på touchenheter.

## Exempel {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
