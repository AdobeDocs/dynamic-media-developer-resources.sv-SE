---
description: Bildmask. Begär maskdata (alfakanal).
solution: Experience Manager
title: mask
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# mask{#mask}

Bildmask. Begär maskdata (alfakanal).

`req=mask`

Stöder samma kommandon som `req=img`. Den bearbetas på samma sätt av servern, men i stället för att data från RGB eller RGBA returneras, ignoreras färginformationen och endast maskdata returneras. MIME-typen för svarsdata och MIME-typen för svar bestäms av `fmt=`.

HTTP-svaret kan nås med TTL-värdet baserat på `catalog::Expiration`.
