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
   <td colname="col2"> <p> Konfigurerar mappningen av enkla klick/tryck för att zooma åtgärder. Om du anger <span class="codeph"> none </span> inaktiveras zoomning med ett enda klick/tryck. Om inställningen är <span class="codeph"> zoomning </span>, zoomas bilden in i ett zoomsteg, om du klickar på bilden zoomas Ctrl+klickar du ett zoomsteg. Om du anger <span class="codeph"> reset </span> återställs zoomningen till den ursprungliga zoomnivån med ett enda klick på bilden. För <span class="codeph"> zoomReset </span> används reset om den aktuella zoomfaktorn är vid eller över den angivna gränsen, i annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-edcfcd6c0bd24ac093442c56450b3c97}

Valfritt.

## Standard {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` på stationära datorer; `none` på touchenheter.

## Exempel {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
