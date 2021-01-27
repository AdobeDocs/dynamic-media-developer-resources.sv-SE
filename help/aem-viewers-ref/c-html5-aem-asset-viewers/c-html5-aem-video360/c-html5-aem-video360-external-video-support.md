---
description: Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller AEM Dynamic Media.
solution: Experience Manager
title: Stöd för extern video
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Stöd för extern video{#external-video-support}

Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller AEM Dynamic Media.

De format som stöds för den externa videon är antingen MP4 i H.264-format eller M3U8-manifest för HLS-ström.

Visningsprogrammet kan arbeta med antingen Dynamic Media Classic- eller AEM Dynamic Media-video eller med extern video. Om visningsprogrammet startar med Dynamic Media Classic/AEM Dynamic Media-video bör det användas med den resurstypen. Det går inte att läsa in en extern video i det här visningsprogrammet med metoden [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) och vice versa. Det vill säga, om visningsprogrammet först lästes in med extern video fortsätter det bara att fungera med externa videor.

När du arbetar med extern video ignorerar visningsprogrammet värdet för alla uppspelningsmodifierare och identifierar uppspelningstypen från det externa videotillägget. Om den externa video-URL:en slutar med `.m3u8` använder visningsprogrammet HLS-uppspelning; I annat fall används progressiv uppspelning.
