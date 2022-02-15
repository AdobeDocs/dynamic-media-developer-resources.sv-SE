---
title: Stöd för extern video
description: Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Stöd för extern video{#external-video-support}

Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller Adobe Experience Manager - Dynamic Media.

De format som stöds för den externa videon är antingen MP4 i H.264-format eller M3U8-manifest för HLS-ström.

Visningsprogrammet kan arbeta med antingen Dynamic Media Classic eller Experience Manager - Dynamic Media eller med extern video. Om visningsprogrammet startar med Dynamic Media Classic/Dynamic Media-video kan du använda det med en sådan resurstyp som fortsätter, men det går inte att läsa in en extern video i visningsprogrammet med [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) -metod. Och tvärtom: om visningsprogrammet först lästes in med extern video bör det bara fortsätta att arbeta med externa videor.

När du arbetar med extern video ignorerar visningsprogrammet värdet för uppspelningsmodifieraren och identifierar uppspelningstypen från det externa videotillägget. Om den externa video-URL:en slutar med `.m3u8` visningsprogrammet använder HLS-uppspelning, annars används progressiv uppspelning.
