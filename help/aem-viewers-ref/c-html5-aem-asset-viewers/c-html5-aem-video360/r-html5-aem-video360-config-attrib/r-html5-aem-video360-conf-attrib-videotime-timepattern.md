---
description: Konfigurationsattribut för Video360 Viewer.
seo-description: Konfigurationsattribut för Video360 Viewer.
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: fe145e6f-742e-44fc-b225-187a86b6700e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoTime.timepattern{#videotime-timepattern}

Konfigurationsattribut för Video360 Viewer.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Anger mönstret för den tid som visas i kontrollfältet, där <span class="codeph"> h</span> är timmar, <span class="codeph"> m</span> är minuter och <span class="codeph"> s</span> är sekunder. </p> <p>Antalet bokstäver som används för varje tidsenhet avgör antalet siffror som ska visas för enheten. Om talet inte får plats i de angivna siffrorna visas motsvarande värde i den efterföljande enheten. </p> <p>Om den aktuella filmtiden till exempel är 67 minuter och 5 sekunder visas tidsmönstret <span class="codeph"> m:ss</span> som 67:05. Samma tid visas som 1:07:5 om det angivna tidsmönstret är <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```

