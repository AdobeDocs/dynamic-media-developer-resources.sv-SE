---
title: Begäranden om kapslad bildåtergivning
description: För avancerade program är det möjligt att använda resultatet av en återgivningsåtgärd som en materialbild, precis som en bild som hämtats från bildservern.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Begäranden om kapslad bildåtergivning{#nested-image-rendering-requests}

För avancerade program är det möjligt att använda resultatet av en återgivningsåtgärd som en materialbild, precis som en bild som hämtats från bildservern.

En återgivningsbegäran kan användas som en materialbild genom att ange den i kommandot `src=` enligt följande:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Token `ir` är skiftlägeskänslig.

Den kapslade begäran får inte innehålla rotsökvägen för bildåtergivning (vanligtvis `http:// *[!DNL server]*/ir/render/'`), men kan innehålla förbearbetningsregeltoken.

Följande kommandon ignoreras när de anges i kapslade begäranden (antingen i begäran-URL:en eller i `catalog::Modifier` eller `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

`attribute::MaxPix` och `attribute::DefaultPix` av materialkatalogen som gäller för den kapslade återgivningsbegäran ignoreras också.

Bildresultatet av en kapslad IR-begäran kan cachelagras genom att inkludera `cache=on`. Som standard är cachelagring av mellanliggande data inaktiverad. Cachelagring bör endast aktiveras när den mellanliggande bilden återanvänds i en annan begäran inom en rimlig tidsperiod. Standardhantering av cacheminnet på serversidan gäller. Data cachelagras i ett förlustfritt format.
