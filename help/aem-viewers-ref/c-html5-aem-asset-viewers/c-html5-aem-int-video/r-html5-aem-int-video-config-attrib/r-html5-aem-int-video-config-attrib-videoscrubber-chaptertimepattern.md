---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: VideoScrubber.chaptertimepattern
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
topic: Dynamic media
uuid: bb021ecb-e169-4cf1-b121-7289311353ed
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Konfigurationsattribut för Interactive Video Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Anger mönstret för den tid som visas i namnlisten i kapiteltabellen, där <span class="codeph"> h</span> representerar timmar, <span class="codeph"> m</span> för minuter och <span class="codeph"> s</span> för sekunder. </p> <p>Antalet bokstäver som används för varje tidsenhet avgör antalet siffror som ska visas för enheten. Om talet inte får plats i de angivna siffrorna visas motsvarande värde i den efterföljande enheten. </p> <p>Om den aktuella filmtiden till exempel är 67 minuter och 5 sekunder visas ett tidsmönster på <span class="codeph"> m:ss</span> som 67:05. Samma tid visas som 1:07:5 om tidsmönstret är <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```

