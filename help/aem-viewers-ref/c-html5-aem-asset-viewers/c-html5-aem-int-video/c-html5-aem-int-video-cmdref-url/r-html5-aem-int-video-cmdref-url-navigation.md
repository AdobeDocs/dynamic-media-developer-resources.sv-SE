---
description: URL-kommando för Interactive Video Viewer.
solution: Experience Manager
title: navigering
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Interaktiva videoklipp
role: Utvecklare,Affärsledare
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 1%

---

# navigering{#navigation}

URL-kommando för Interactive Video Viewer.

` navigation= *`fil`*`

Visningsprogrammet har stöd för kapitelnavigering via WebVTT-filer på webben. Cue-positioneringsoperatorer stöds inte.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fil</span> </span> </p> </td> 
   <td colname="col2"> <p> Anger en URL eller sökväg till WebVTT-navigeringsinnehåll. Image Serving bör vara värd för WebVTT-filen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Ingen.

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```
