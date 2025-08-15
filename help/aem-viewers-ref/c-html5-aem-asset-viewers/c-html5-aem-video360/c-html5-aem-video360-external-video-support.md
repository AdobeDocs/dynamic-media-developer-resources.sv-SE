---
title: Stöd för extern video
description: Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Stöd för extern video{#external-video-support}

Visningsprogrammet stöder uppspelning av video som ligger utanför Dynamic Media Classic eller Adobe Experience Manager, Dynamic Media.

De format som stöds för den externa videon är antingen MP4 i H.264-format eller M3U8-manifest för HLS-ström.

Visningsprogrammet kan arbeta med antingen Dynamic Media Classic eller Experience Manager Dynamic Media eller med extern video. Om visningsprogrammet startar med Dynamic Media Classic/AEM Dynamic Media-videon bör den användas med en sådan resurstyp som fortsätter. Det går inte att läsa in en extern video i det här visningsprogrammet med metoden [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) och omvänt. Det vill säga, om visningsprogrammet först lästes in med extern video fortsätter det bara att fungera med externa videor.

När du arbetar med extern video ignorerar visningsprogrammet värdet för alla uppspelningsmodifierare och identifierar uppspelningstypen från det externa videotillägget. Om den externa video-URL:en slutar med `.m3u8` använder visningsprogrammet HLS uppspelning, annars används progressiv uppspelning.
