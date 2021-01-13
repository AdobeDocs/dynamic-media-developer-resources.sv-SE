---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
topic: Dynamic media
uuid: 7496fea1-8a69-4749-ab4b-ae6d375441b8
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 2%

---


# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Kommandosträngen Bildrutevisning som används på alla miniatyrbilder. Om det anges i URL:en måste alla förekomster av <span class="codeph"> &amp;</span> och <span class="codeph"> =</span> vara HTTP-kodade som <span class="codeph"> %26</span> respektive <span class="codeph"> %3D</span>. </p> </td> 
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
