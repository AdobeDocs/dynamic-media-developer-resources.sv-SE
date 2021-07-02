---
description: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,Business Practitioner
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ingen|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Bilden som ska visas i den första bildrutan innan videon börjar spelas upp, matchas mot <span class="codeph"> serverurl</span>. Om det anges i URL:en, HTTP-kodar du följande: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> som  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> som  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> som  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Om <span class="codeph"><span class="varname"> image_id</span></span>-värdet utelämnas försöker komponenten använda standardförhandsvisningsbilden för den resursen i stället. </p> <p>När videon har angetts som en sökväg hämtas standardfilens katalog-ID från videosökvägen som <span class="codeph"> catalog_id/image_id</span>-paret där <span class="codeph"> catalog_id</span> motsvarar den första token i sökvägen och <span class="codeph"> image_id</span> är namnet på videon där tillägget har tagits bort. Om bilden med detta ID inte finns visas inte förhandsvisningsbilden. </p> <p>Om du vill förhindra att standardförhandsvisningsbilden visas anger du <span class="codeph"> none</span> som värde för förhandsvisningsbilden. Om bara <span class="codeph"><span class="varname"> isCommands</span></span> anges används kommandona på standardförhandsvisningsbilden innan bilden visas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Ingen.

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
