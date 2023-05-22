---
title: FlyoutZoomView.iscommand
description: FlyoutZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2ae17dc8-2728-4ee5-ba88-45d78a0f4d9a
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>Kommandosträngen Bildsökning som används på huvudbilden för FlyoutZoomView och den inzoomade vyn. Om den anges i URL:en måste du se till att du kodar alla förekomster av <span class="codeph"> &amp;</span> och <span class="codeph"> =</span> as <span class="codeph"> %26</span> och <span class="codeph"> %3D</span>, respektive. </p> <p> <p>Obs! Kommandon för att ändra bildstorlek stöds inte. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

Ingen.

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

När det anges i visningsprogrammets URL:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

När det anges i konfigurationsdata:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
