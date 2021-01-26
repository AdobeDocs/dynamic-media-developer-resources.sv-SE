---
description: För avancerade program är det möjligt att använda resultatet av en återgivningsåtgärd som en materialavbildning, precis som en bild som hämtats från Image Serving.
seo-description: För avancerade program är det möjligt att använda resultatet av en återgivningsåtgärd som en materialavbildning, precis som en bild som hämtats från Image Serving.
seo-title: Begäranden om kapslad bildåtergivning
solution: Experience Manager
title: Begäranden om kapslad bildåtergivning
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Begäranden om kapslad bildåtergivning{#nested-image-rendering-requests}

För avancerade program är det möjligt att använda resultatet av en återgivningsåtgärd som en materialavbildning, precis som en bild som hämtats från Image Serving.

En renderingsbegäran kan användas som en materialavbildning genom att ange den i kommandot `src=` enligt följande:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Token `ir` är skiftlägeskänslig.

Den kapslade begäran får inte innehålla rotsökvägen för bildåtergivning (vanligtvis `http:// *[!DNL server]*/ir/render/'`), men kan innehålla token för förbearbetningsregel.

Följande kommandon ignoreras när de anges i kapslade begäranden (antingen i begäran-URL:en eller i `catalog::Modifier` eller `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Även `attribute::MaxPix` och `attribute::DefaultPix` ignoreras för materialkatalogen som gäller för den kapslade återgivningsbegäran.

Bildresultatet av en kapslad IR-begäran kan cachelagras genom att inkludera `cache=on`. Som standard är cachelagring av mellanliggande data inaktiverad. Cachelagring bör endast aktiveras när den mellanliggande bilden förväntas återanvändas i en annan begäran inom en rimlig tidsperiod. Standardhantering av cache på serversidan gäller. Data cachelagras i ett icke-förstörande format.
