---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfigurerar mappningen av enkla klick/tryck för att zooma åtgärder. Om du anger <span class="codeph"> inget </span> inaktiveras zoomning med en klickning. Om den är inställd på <span class="codeph"> zoomning </span> när du klickar på bilden zoomas den i ett zoomsteg; CTRL+Click zoomar ut ett zoomsteg. Om du anger <span class="codeph"> reset </span> återställs zoomningen till den ursprungliga zoomnivån med ett enda klick på bilden. För <span class="codeph"> zoomReset </span> används reset om den aktuella zoomfaktorn är vid eller över den angivna gränsen, i annat fall används zoomning. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-edcfcd6c0bd24ac093442c56450b3c97}

Valfritt.

## Standard {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] på stationära datorer,  [!DNL `none`] på pekenheter.

## Exempel {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]