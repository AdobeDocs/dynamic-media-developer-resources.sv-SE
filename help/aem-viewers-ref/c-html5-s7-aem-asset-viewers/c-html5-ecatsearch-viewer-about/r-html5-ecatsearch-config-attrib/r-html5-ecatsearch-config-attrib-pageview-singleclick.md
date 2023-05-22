---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av enkla klick/tryck för att zooma åtgärder. Inställning till <span class="codeph"> ingen </span> Inaktiverar zoomning med ett enda klick/tryck. Om inställt på <span class="codeph"> zooma </span> klicka på bilden zoomas in ett zoomsteg, CTRL+Click zoomar ut ett zoomsteg. Inställning till <span class="codeph"> återställ </span> gör att ett enda klick på bilden återställer zoomningen till den ursprungliga zoomnivån. För <span class="codeph"> zoomReset </span>återställs om den aktuella zoomfaktorn är på eller utanför den angivna gränsen. I annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-edcfcd6c0bd24ac093442c56450b3c97}

Valfritt.

## Standard {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] på stationära datorer, [!DNL `none`] på pekenheter.

## Exempel {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
