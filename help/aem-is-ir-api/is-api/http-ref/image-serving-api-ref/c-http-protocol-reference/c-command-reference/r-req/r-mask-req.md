---
description: Bildmask. Begär maskdata (alfakanal).
solution: Experience Manager
title: mask
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# mask{#mask}

Bildmask. Begär maskdata (alfakanal).

`req=mask`

Stöder samma kommandon som `req=img`. Den bearbetas på samma sätt av servern, men i stället för att returnera RGB- eller RGBA-data tar servern bort färginformationen och returnerar bara maskdata (alfakanaler). MIME-typen för svarsdataformat och svar bestäms av `fmt=`.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.
