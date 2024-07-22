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

Ange begäran i kommandot `src=` enligt följande:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Token `is` är skiftlägeskänslig.

Den kapslade begäran får inte innehålla rotsökvägen för bildservrar (vanligtvis  [!DNL http:// *[!DNL server]*/is/image/"]), men kan innehålla token för förbearbetningsregel.

Följande IS-kommandon ignoreras när de anges i kapslade begäranden (antingen i begärande-URL eller i `catalog::Modifier` eller `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

`attribute::MaxPix` och `attribute::DefaultPix` av bildkatalogen som gäller för den inbäddade IS-begäran ignoreras också.

Om resultatbilden för den kapslade begäran innehåller maskdata (alfa) skickas den alltid till materialet. Använd ett enfärgat bakgrundsbildlager för att undvika oönskad alfa.

Bildresultatet av en inbäddad IS-begäran kan cachelagras genom att inkludera `cache=on`. Som standard är cachelagring av mellanliggande data inaktiverad. Cachelagring bör endast aktiveras när den mellanliggande bilden återanvänds i en annan begäran inom en rimlig tidsperiod. Standardhantering av cacheminnet på serversidan gäller. Data cachelagras i ett förlustfritt format.
