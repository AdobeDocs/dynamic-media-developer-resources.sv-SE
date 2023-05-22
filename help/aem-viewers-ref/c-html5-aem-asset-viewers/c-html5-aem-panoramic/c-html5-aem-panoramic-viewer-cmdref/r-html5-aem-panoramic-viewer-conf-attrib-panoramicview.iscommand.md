---
title: PanoramicView.iscommand
description: Konfigurationsattribut för panoramavisningsprogram.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

Konfigurationsattribut för panoramavisningsprogram.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Kommandosträngen Bildrutevisning som används på bilden.  Om den anges i URL:en måste du se till att du kodar alla förekomster av <span class="codeph"> &amp;</span> och <span class="codeph"> =</span> as <span class="codeph"> %26</span> och <span class="codeph"> %3D</span>, respektive. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Ingen standard.

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

När det anges i visningsprogrammets URL.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

När det anges i konfigurationsdata.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
