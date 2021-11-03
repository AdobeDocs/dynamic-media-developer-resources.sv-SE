---
description: Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller AEM Dynamic Media.
solution: Experience Manager
title: Stöd för extern video
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Stöd för extern video{#external-video-support}

Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller AEM Dynamic Media.

De format som stöds för den externa videon är antingen MP4 i H.264-format eller M3U8-manifest för HLS-ström.

Visningsprogrammet kan arbeta med antingen Dynamic Media Classic- eller AEM Dynamic Media-video eller extern video. Om visningsprogrammet startar med Dynamic Media Classic/Dynamic Media-video kan du använda det med en sådan resurstyp som fortsätter, men det går inte att läsa in en extern video i visningsprogrammet med [ `setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Och tvärtom: om visningsprogrammet först lästes in med extern video bör det bara fortsätta att arbeta med externa videor.

När du arbetar med extern video ignorerar visningsprogrammet värdet för uppspelningsmodifieraren och identifierar uppspelningstypen från det externa videotillägget. Om den externa video-URL:en slutar med .m3u8 använder visningsprogrammet HLS-uppspelning, annars används progressiv uppspelning.
