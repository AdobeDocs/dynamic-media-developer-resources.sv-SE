---
description: Konfigurationsattribut för Video Viewer.
solution: Experience Manager
title: EmbedShare.embedsizes
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Video
role: Developer,User
exl-id: cf075711-1275-4eb2-8cb6-fb2609711c7a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 3%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Konfigurationsattribut för Video Viewer.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *``*, *``*[,0|1][; *``*, *`breddhöjdbreddhöjd`*[,0|1]]`

Anger en lista med inbäddningsstorlekar för kombinationsrutan för storlek i dialogrutan för inbäddningsdelning.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width  </span> </span> </p> </td> 
   <td colname="col2"> <p> Bädda in bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height  </span> </span> </p> </td> 
   <td colname="col2"> <p>Bädda in höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Anger om det här listobjektet ska vara förmarkerat i kombinationsrutan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
