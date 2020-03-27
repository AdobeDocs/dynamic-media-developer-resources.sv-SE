---
description: 'null'
seo-description: 'null'
seo-title: PageView.singleClick
solution: Experience Manager
title: PageView.singleClick
topic: Dynamic media
uuid: 608700d2-5be4-4b96-b026-b12a3ade68ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.singleClick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av enkla klick/tryck för att zooma åtgärder. Om du väljer <span class="codeph"> Ingen </span> inaktiveras zoomning med ett enda klick/tryck. Om inställningen är att <span class="codeph"> zooma in </span> zoomningen zoomas bilden i ett zoomsteg, CTRL+Click zoomar ut ett zoomsteg. Om du anger att du vill <span class="codeph"> återställa bilden </span> återställs zoomningen till den ursprungliga zoomnivån med ett enda klick. För <span class="codeph"> zoomReset </span>används reset om den aktuella zoomfaktorn är på eller över den angivna gränsen, i annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-edcfcd6c0bd24ac093442c56450b3c97}

Valfritt.

## Standard {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` på stationära datorer, på `none` pekenheter.

## Exempel {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
