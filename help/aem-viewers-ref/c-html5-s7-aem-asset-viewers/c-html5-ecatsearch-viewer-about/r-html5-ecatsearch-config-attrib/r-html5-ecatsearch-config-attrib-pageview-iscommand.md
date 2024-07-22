---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fd1fa0f2-d666-4470-8b5b-673f3c4327e0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---

# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand </span></span> </p> </td> 
   <td colname="col2"> <p> Kommandosträngen Bildrutevisning som används på sidbilden. Om det anges i URL:en måste alla förekomster av <span class="codeph"> &amp;</span> och <span class="codeph"> =</span> vara HTTP-kodade som <span class="codeph"> %26</span> respektive <span class="codeph"> %3D</span>. </p> <p> <p>Obs! Kommandon för att ändra bildstorlek stöds inte. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-df5a0604766b4ac2b9a6742b377e427c}

Valfritt.

## Standard {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Ingen.

## Exempel {#section-813de2905d6c44c0991cfe0931581462}

När det anges i visningsprogrammets URL.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

När det anges i konfigurationsdata.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
