---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Textbunden zoom
role: Developer,User
exl-id: b5b0acab-4e11-4f6a-8cb1-be6d683d7384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 1%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Kommandosträngen Bildrutehantering som används för alla färgrutor. Om den anges i URL:en måste du HTTP-koda alla förekomster av <span class="codeph"> &amp;</span> och <span class="codeph"> =</span> som <span class="codeph"> %26</span> respektive <span class="codeph"> %3D</span>. </p> <p> <p>Obs!  Kommandon för att ändra bildstorlek stöds inte. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-e6310c8c4e8547689a5b48ceddb3671d}

Valfritt.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

Ingen.

## Exempel {#section-3a188ab955c445bcb2efa3c49722c10d}

När det anges i visningsprogrammets URL.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

När det anges i konfigurationsdata.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
