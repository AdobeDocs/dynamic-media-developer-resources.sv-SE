---
title: SmartCropVideoPlayer.posterimage
description: Konfigurationsattribut för visningsprogrammet för smart beskärning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ff4f8e2c-b9c3-4fba-b3f0-fa1eaddcd8c0
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

Konfigurationsattribut för visningsprogrammet för smart beskärning.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Bilden som ska visas i den första bildrutan innan videon börjar spelas upp, matchas mot <span class="codeph"> server</span>. Om det anges i URL:en, HTTP-kodar du följande: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> som <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> som <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Om värdet <span class="codeph"><span class="varname"> image_id</span></span> utelämnas försöker komponenten använda standardförhandsvisningsbilden för den resursen i stället. </p> <p>När videon har angetts som en sökväg hämtas standardfilens katalog-ID från videosökvägen som <span class="codeph"> catalog_id/image_id</span> -paret. <span class="codeph"> catalog_id </span> motsvarar den första token i sökvägen och <span class="codeph"> image_id </span> är namnet på videon med tillägget borttaget. Om bilden med detta ID inte finns visas inte förhandsvisningsbilden. </p> <p>Om du vill förhindra att standardförhandsvisningsbilden visas anger du <span class="codeph"> none</span> som värde för förhandsvisningsbilden. Om bara <span class="codeph"><span class="varname"> isCommands</span></span> anges används kommandona på standardförhandsvisningsbilden innan bilden visas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Ingen.

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
