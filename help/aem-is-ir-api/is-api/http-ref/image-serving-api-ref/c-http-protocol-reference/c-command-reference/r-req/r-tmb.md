---
description: Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.
seo-description: Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.
seo-title: tmb
solution: Experience Manager
title: tmb
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# tmb{#tmb}

Miniatyrbild. Begär bilddata som är formaterade och storleksanpassade med hjälp av katalogminiatyrvillkor.

`req=tmb`

MIME-typen för svarsdataformat och svar bestäms av `fmt=`. Stöder alla kommandon utom `fit=`.

Se [Skala för miniatyrbilder](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

HTTP-svaret kan cachas med TTL-värdet baserat på `catalog::Expiration`.
