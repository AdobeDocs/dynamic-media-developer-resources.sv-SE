---
title: Inbäddade bildserverbegäranden
description: En Image Server-begäran (IS) kan användas som en materialavbildning.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Inbäddade bildserverbegäranden{#embedded-image-server-requests}

En Image Server-begäran (IS) kan användas som en materialavbildning.

Ange begäran i dialogrutan `src=` enligt följande:

` …&src=is( *[!DNL imageServingRequest]*)&…`

The `is` är skiftlägeskänslig.

Den kapslade begäran får inte innehålla rotsökvägen för bildservern (vanligtvis [!DNL http:// *[!DNL server]*/is/image/"]), men kan inkludera förbearbetningsregeltoken.

Följande IS-kommandon ignoreras när de anges i kapslade begäranden (antingen i begärande-URL eller i `catalog::Modifier` eller `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Även ignorerade `attribute::MaxPix` och `attribute::DefaultPix` för den bildkatalog som gäller för den inbäddade IS-begäran.

Om resultatbilden för den kapslade begäran innehåller maskdata (alfa) skickas den alltid till materialet. Använd ett enfärgat bakgrundsbildlager för att undvika oönskad alfa.

Bildresultatet av en inbäddad IS-begäran kan cachas genom att inkludera `cache=on`. Som standard är cachelagring av mellanliggande data inaktiverad. Cachelagring bör endast aktiveras när den mellanliggande bilden återanvänds i en annan begäran inom en rimlig tidsperiod. Standardhantering av cache på serversidan gäller. Data cachelagras i ett icke-förstörande format.
