---
description: Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller AEM Dynamic Media.
solution: Experience Manager
title: Stöd för extern video
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Video
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Stöd för extern video{#external-video-support}

Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller AEM Dynamic Media.

De format som stöds för den externa videon är antingen MP4 i H.264-format eller M3U8-manifest för HLS-ström.

Visningsprogrammet kan arbeta med antingen Dynamic Media Classic- eller AEM Dynamic Media-video eller med extern video. Om visningsprogrammet startar med en Dynamic Media Classic/Dynamic Media-video kan du använda den med den resurstypen framåt. Det går inte att läsa in en extern video i visningsprogrammet med metoden [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Och tvärtom: om visningsprogrammet först lästes in med extern video bör det bara fortsätta att arbeta med externa videor.

När du arbetar med extern video ignorerar visningsprogrammet värdet för uppspelningsmodifieraren och identifierar uppspelningstypen från det externa videotillägget. Om den externa video-URL:en slutar med .m3u8 använder visningsprogrammet HLS-uppspelning, annars används progressiv uppspelning.
