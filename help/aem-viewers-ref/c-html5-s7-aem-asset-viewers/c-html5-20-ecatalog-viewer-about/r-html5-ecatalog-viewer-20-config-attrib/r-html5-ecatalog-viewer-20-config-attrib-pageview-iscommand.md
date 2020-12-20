---
description: 'null'
seo-description: 'null'
seo-title: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
topic: Dynamic media
uuid: 6c853c6a-a57d-4cab-ad71-74baf9e870d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 1%

---


# PageView.iscommand{#pageview-iscommand}

` [PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Kommandosträngen Bildrutevisning som används på sidbilden. Om det anges i URL:en måste alla förekomster av <span class="codeph"> &amp;</span> och <span class="codeph"> =</span> vara HTTP-kodade som <span class="codeph"> %26</span> respektive <span class="codeph"> %3D</span>. </p> <p> <p>Obs!  Kommandon för att ändra bildstorlek stöds inte. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-df5a0604766b4ac2b9a6742b377e427c}

Valfritt.

## Standard {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Ingen.

## Exempel {#section-813de2905d6c44c0991cfe0931581462}

När det anges i visningsprogrammets URL.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

När det anges i konfigurationsdata.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
