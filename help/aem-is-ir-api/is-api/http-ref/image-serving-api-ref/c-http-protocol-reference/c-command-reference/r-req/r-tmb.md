---
description: Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.
seo-description: Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# tmb{#tmb}

Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.

`req=tmb`

MIME-typen för svarsdataformat och svar bestäms av `fmt=`. Stöder alla kommandon utom `fit=`.

Se [Skala för miniatyrbilder](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

HTTP-svaret kan cachas med TTL-värdet baserat på `catalog::Expiration`.
