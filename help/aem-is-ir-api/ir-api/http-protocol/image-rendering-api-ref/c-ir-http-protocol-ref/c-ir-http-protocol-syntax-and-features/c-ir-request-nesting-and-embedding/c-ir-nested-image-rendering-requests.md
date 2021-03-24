---
description: För avancerade program är det möjligt att använda resultatet av en återgivningsåtgärd som en materialavbildning, precis som en bild som hämtats från Image Serving.
solution: Experience Manager
title: Begäranden om kapslad bildåtergivning
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '198'
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
