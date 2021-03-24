---
description: En Image Server-begäran (IS) kan användas som en materialavbildning.
solution: Experience Manager
title: Inbäddade bildserverbegäranden
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Inbäddade bildserverbegäranden{#embedded-image-server-requests}

En Image Server-begäran (IS) kan användas som en materialavbildning.

Ange begäran i kommandot `src=` enligt följande:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Token `is` är skiftlägeskänslig.

Den kapslade begäran får inte innehålla sökvägen till Image Serving-roten (vanligtvis [!DNL http:// *[!DNL server]*/is/image/&quot;]), men kan innehålla token för förbearbetningsregel.

Följande IS-kommandon ignoreras när de anges i kapslade begäranden (antingen i begärande-URL eller i `catalog::Modifier` eller `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Även `attribute::MaxPix` och `attribute::DefaultPix` för bildkatalogen som gäller för den inbäddade IS-begäran ignoreras.

Om resultatbilden för den kapslade begäran innehåller maskdata (alfa) skickas den alltid till materialet. Använd ett enfärgat bakgrundsbildlager för att undvika oönskad alfa.

Bildresultatet av en inbäddad IS-begäran kan cachelagras genom att inkludera `cache=on`. Som standard är cachelagring av mellanliggande data inaktiverad. Cachelagring bör endast aktiveras när den mellanliggande bilden förväntas återanvändas i en annan begäran inom en rimlig tidsperiod. Standardhantering av cache på serversidan gäller. Data cachelagras i ett icke-förstörande format.
