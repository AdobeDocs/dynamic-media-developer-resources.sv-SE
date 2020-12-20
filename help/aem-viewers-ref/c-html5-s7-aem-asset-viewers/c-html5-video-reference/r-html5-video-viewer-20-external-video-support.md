---
description: Visningsprogrammet har stöd för uppspelning av video som lagras utanför Scene7 Publishing System eller AEM Dynamic Media.
seo-description: Visningsprogrammet har stöd för uppspelning av video som lagras utanför Scene7 Publishing System eller AEM Dynamic Media.
seo-title: Stöd för extern video
solution: Experience Manager
title: Stöd för extern video
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Stöd för extern video{#external-video-support}

Visningsprogrammet har stöd för uppspelning av video som lagras utanför Scene7 Publishing System eller AEM Dynamic Media.

De format som stöds för den externa videon är antingen MP4 i H.264-format eller M3U8-manifest för HLS-ström.

Visningsprogrammet kan arbeta med antingen Scene7- eller Dynamic Media-video eller extern video. Om visningsprogrammet startar med Scene7/Dynamic Media-video kan du använda det med en sådan resurstyp som fortsätter, men det går inte att läsa in en extern video i visningsprogrammet med metoden [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Och tvärtom: om visningsprogrammet först lästes in med extern video bör det bara fortsätta att arbeta med externa videor.

När du arbetar med extern video ignorerar visningsprogrammet värdet för uppspelningsmodifieraren och identifierar uppspelningstypen från det externa videotillägget. Om den externa video-URL:en slutar med .m3u8 använder visningsprogrammet HLS-uppspelning, annars används progressiv uppspelning.
