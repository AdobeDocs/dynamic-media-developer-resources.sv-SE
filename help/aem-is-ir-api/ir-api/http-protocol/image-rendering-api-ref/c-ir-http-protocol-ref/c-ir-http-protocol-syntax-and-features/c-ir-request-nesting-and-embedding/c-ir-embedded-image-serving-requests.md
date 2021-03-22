---
description: En Image Server-begäran (IS) kan användas som en materialavbildning.
seo-description: En Image Server-begäran (IS) kan användas som en materialavbildning.
seo-title: Inbäddade bildserverbegäranden
solution: Experience Manager
title: Inbäddade bildserverbegäranden
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '211'
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
