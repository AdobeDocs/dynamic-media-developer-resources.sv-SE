---
description: Bildmask. Begär maskdata (alfakanal).
seo-description: Bildmask. Begär maskdata (alfakanal).
seo-title: mask
solution: Experience Manager
title: mask
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

Bildmask. Begär maskdata (alfakanal).

`req=mask`

Stöder samma kommandon som `req=img`och bearbetas på samma sätt av servern, men i stället för att returnera RGB- eller RGBA-data tar servern bort färginformationen och returnerar bara maskdata (alfakanaler). Svarsdataformatet och MIME-typen för svar bestäms av `fmt=`.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.
