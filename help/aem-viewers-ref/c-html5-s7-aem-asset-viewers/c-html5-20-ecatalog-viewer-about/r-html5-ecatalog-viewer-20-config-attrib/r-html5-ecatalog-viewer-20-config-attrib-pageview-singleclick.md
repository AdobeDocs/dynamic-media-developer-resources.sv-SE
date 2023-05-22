---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

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

`zoomReset` på stationära datorer, `none` på pekenheter.

## Exempel {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
