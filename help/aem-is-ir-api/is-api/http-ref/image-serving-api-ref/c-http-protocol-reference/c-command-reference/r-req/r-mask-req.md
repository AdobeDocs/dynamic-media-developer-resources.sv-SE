---
description: Bildmask. Begär maskdata (alfakanal).
seo-description: Bildmask. Begär maskdata (alfakanal).
seo-title: mask
solution: Experience Manager
title: mask
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# mask{#mask}

Bildmask. Begär maskdata (alfakanal).

`req=mask`

Stöder samma kommandon som `req=img` och bearbetas på samma sätt av servern, men i stället för att returnera RGB- eller RGBA-data, ignorerar servern färginformationen och returnerar bara maskdata (alfakanaler). MIME-typen för svarsdataformat och svar bestäms av `fmt=`.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.
