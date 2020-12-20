---
description: Kommandosträngen Bildrutevisning som används på alla miniatyrbilder.
seo-description: Kommandosträngen Bildrutevisning som används på alla miniatyrbilder.
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
topic: Dynamic media
uuid: be3d49d1-d5d2-4ecd-bc8f-fe5f80204c76
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 1%

---


# FavoritesView.iscommand{#favoritesview-iscommand}

Kommandosträngen Bildrutevisning som används på alla miniatyrbilder.

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Om det anges i URL:en måste alla förekomster av <span class="codeph"> &amp;</span> och <span class="codeph"> =</span> vara HTTP-kodade som <span class="codeph"> %26</span> respektive <span class="codeph"> %3D</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Ingen.

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

När det anges i visningsprogrammets URL.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

När det anges i konfigurationsdata.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
