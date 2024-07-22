---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Anger när informationspanelen ska visas. </p> <p>Om värdet är <span class="codeph"> 1</span> visas informationspanelen när musen kommer in i bildschemaområdet (om bildschemat inte är tomt, <span class="codeph"> rollover_key </span> -attribut). </p> <p>Om <span class="codeph"> 0</span>-informationspanelen anges aktiveras när bildschemat väljs (om bildschemat har ett icke-tomt <span class="codeph"> rollover_key </span> och tomma <span class="codeph"> href </span> -attribut). </p> <p> Ignoreras på pekenheter, inklusive datorer med pekskärm, och ställs automatiskt in på <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-ccfedc2da28f412a86d03f390db92b4b}

Valfritt.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Exempel {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
